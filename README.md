스프링 IoC
=========

## 스프링 IoC(Inversion of Control)
* 일반적인 (의존성에 대한) 제어권: "내가 사용할 의존성은 내가 만든다."
```
class OwnerController {
    private OwnerRespository respository = new OwnerRespository();
}
```
* IoC: "내가 사용할 의존성을 누군가 알아서 주겠지"
    - 내가 사용할 의존성의 타입(또는 인터페이스)만 맞으면 어떤 것이든 상관없다.
    - 코드 테스트가 쉽다.
```
class OwnerController {
    // OwnerRespository를 사용하지만 만들진 않는다.
    private OwnerRespository repo;
    
    public OwnerController(OwnerRespository repo) {
        this.repo = repo;
    }
}
```



## 스프링 IoC 컨테이너
## 스프링 빈(Bean)
## 의존성 주입(Dependency Injection)