# 20220830

### 실전프로젝트 진짜 시작.

주제를 선정하고 초기 계획을 세우는데만 5일 정도의 시간이 걸린 것 같다.

-----

회원가입이 완료 되면 자동으로 메일을 보내게되어   
이메일 인증을 하게 되는 기능을 구현해봤다.

스프링 자체 **JavaMailSender** 기능을 사용했다.

```
dependencies{

implementation 'org.springframework.boot:spring-boot-starter-mail'

}
```
<img src="https://github.com/projectmiluju/TIL/blob/main/202208/20220830/email.PNG" alt="email" width="500"></img><br/>
<img src="https://github.com/projectmiluju/TIL/blob/main/202208/20220830/email.PNG" alt="emailid" width="500"></img><br/>
<img src="https://github.com/projectmiluju/TIL/blob/main/202208/20220830/email.PNG" alt="emailurl" width="500"></img><br/>
