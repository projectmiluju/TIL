# 20220730

## CS STUDY
#### SOFTWARE 20&21<br></br>
#### 10억 개 전화번호에서 이름 찾기 : 이진검색
#### 검색을 쉽게 만드는 정렬 : 선택 정렬 vs 퀵 정렬


### 이진검색 Binary Search (이진탐색)
>정렬된 배열(ex 사전,전화번호부) 에서 검색 범위를 줄여 나가며 검색 값을 찾는 알고리즘   
>검색이 반복될 떄마다 검색 범위가 절반으로 줄어서 속도가 빠르다는 장점   
>정렬된 배열에만 사용할 수 있다는 단점

### 이진검색 동작방식
> 1. 배열의 중간 값을 가져옵니다.
> 2. 중간 값과 검색 값을 비교합니다.   
> 2-1. 중간 값이 검색 값과 같다면 종료합니다.   
> 2-2. 중간 값보다 검색 값이 크다면 중간값 기준 배열의 오른쪽 구간을 탐색합니다.   
> 2-3. 중간 값보다 검색 값이 작다면 중간갑 기준 배열의 왼쪽 구간을 탐색합니다.
> 3. 값을 찾거나 간격이 비어있을 때까지 반복합니다.

>### 이진검색 vs 선형검색   
>배열 {1,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59} 에서 37 찾기
<img src="https://velog.velcdn.com/images/hongsoom/post/32334a8a-e6f2-4004-8b7e-fd6123e37a5b/image.gif" width="1000" alt="이진검색"></img>

### 이진검색 성능
><img src="https://velog.velcdn.com/images/hongsoom/post/18d94ff0-9d43-4727-8c81-83a7db188a2f/image.PNG" width="500" alt="퀵정렬"></img>

### 선택정렬
>배열의 모든 요소를 앞에서부터 차례대로이미정렬
> 
<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FkLXa2%2FbtqHT0KD0Nq%2FvMuJzpTY5fGciZqmGpNvh1%2Fimg.png" width="1000" alt="선택정렬"></img>

### 퀵정렬
<img src="https://gmlwjd9405.github.io/images/algorithm-quick-sort/quick-sort.png" width="1000" alt="퀵정렬"></img>
### 퀵정렬 시간복잡도
<img src="https://gmlwjd9405.github.io/images/algorithm-quick-sort/sort-time-complexity-etc1.png" width="1000" alt="퀵정렬시간 복잡도"></img>

>선택정렬은 단순하지만 비효울적인 방법   
>퀵정렬은 복잡하지만 효울적인 방법