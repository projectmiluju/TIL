# 20220903

### SWAGGER

실전프로젝트에 SWAGGER를 연동 하려고한 과정에서 생긴 에러이다.

<img src="https://github.com/projectmiluju/TIL/blob/main/202209/20220909/%EC%8A%A4%EC%9B%A8%EA%B1%B0%EC%98%A4%EB%A5%98.PNG" alt="SwaggerError" width="1000"></img><br/>

>Failed to start bean 'documentationPluginsBootstrapper';   

현재 프로젝트에서 사용하는   
springboot 버전은 2.7.3   
swagger 버전은 2.9.2    

Spring Boot 2.6 이상 버전 부터는 spring.mvc.pathmatch.matching-strategy 값이 ant_apth_matcher에서 path_pattern_parser로 변경되어 오류가 발생하고 있다.   
해결방법은 간단하다.
```
spring.mvc.pathmatch.matching-strategy=ant_path_matcher
```
application.properties에 추가 해주기만하면 된다.