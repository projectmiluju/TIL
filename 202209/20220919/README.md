# 20220909

### Transactional

#### Transaction
> Transaction이란 데이터베이스에서 데이터에 대한 하나의 논리적 실행단계이다.


#### @Transactional

        @Transactional
        public ResponseEntity<?> getRank(@AuthenticationPrincipal UserDetails user, int pageNum, int size) {
        pageNum = pageNum - 1;
        Pageable pageable = PageRequest.of(pageNum, size);
        Slice<Member> allByOrderByPointsDesc = memberRepository.rank(pageable);


        List<RankPageDto> rankPageDtos = new ArrayList<>();

        for (Member member : allByOrderByPointsDesc) {
            List<Long> levelAndPoint = levelCheck.levelAndPoint(member.getNickname());
            List<Long> sevengraph = graph.SevenDaysGraph(member.getNickname());
            rankPageDtos.add(RankPageDto.builder()
                    .id(member.getId())
                    .profileImg(member.getProfileImg())
                    .level(levelAndPoint.get(1) + "LV")
                    .nickname(member.getNickname())
                    .score(member.getPoints())
                    .graph(sevengraph)
                    .build());
        }
        if (user != null) {
            for (int i = 0; i < rankPageDtos.size(); i++) {
                if (user.getUsername().equals(rankPageDtos.get(i).getNickname())) {
                    System.out.println(i + 1);
                    int myRank = i + 1;
                    String nickname = rankPageDtos.get(i).getNickname();
                    memberRepository.updateRank(myRank, nickname);
                }
            }
        }

        System.out.println(member.get().getMyRank());

        return ResponseEntity.ok().body(Map.of("msg", "랭킹 조회 완료", "data", rankPageDtos));
        }

이번 실전 프로젝트에서 각 유저의 랭킹을 구해 저장해주는 코드이다.   
랭크를 잘 계산해서 출력까지 했지만 @Transactional 어노테이션을 달아주지 않아   
저장되지 않고 실행되지 않아서 한참을 어처구니없이 해매고 말았다.

>@Transactional