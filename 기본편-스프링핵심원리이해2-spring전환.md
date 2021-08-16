기본편 - 스프링핵심원리이해2

## AppConfig 리팩토링

<img width="571" alt="1" src="https://user-images.githubusercontent.com/52316270/129543387-0dd47ca4-4e3d-469c-b1ae-d87f337d7201.png">

기대하는 그림과 달리 무슨 역할을하는지 자세히는 모른다

따라서 역할을 한 눈에 알 수 있도록 바꿔줘야 한다.

<img width="603" alt="2" src="https://user-images.githubusercontent.com/52316270/129543402-e3aa884c-497c-413b-a6bf-e972a3eee889.png">

MemberRepository, discountPolicy를 따로 제작하여 역할을 보여주었다.

결론

<img width="595" alt="3" src="https://user-images.githubusercontent.com/52316270/129543428-d0964aaa-7257-4374-b8e2-2ae74dc1048f.png">


## 정액할인 정책을 정률할인 정책으로 변경

<img width="554" alt="4" src="https://user-images.githubusercontent.com/52316270/129543457-58b807a1-7f3b-421a-9ac0-555addfcf447.png">

->구성영역만 변경하면 된다.



## 여기서 적용된 Solid원칙

<img width="561" alt="5" src="https://user-images.githubusercontent.com/52316270/129543509-bcf29a4c-f3ba-43d8-800c-b0d0887143cf.png">

<img width="555" alt="6" src="https://user-images.githubusercontent.com/52316270/129543527-04168c5e-937b-4cf0-8939-338265db1882.png">


## IoC, DI, 컨테이너

<img width="568" alt="7" src="https://user-images.githubusercontent.com/52316270/129543547-aabd3aa0-c095-4cbe-9eaf-22f6102e4540.png">

<img width="546" alt="8" src="https://user-images.githubusercontent.com/52316270/129543568-56264d71-d529-4407-99f8-b83677e27c32.png">

<img width="489" alt="9" src="https://user-images.githubusercontent.com/52316270/129543589-8067db3f-c2d4-4cf5-a18a-46c2739d5465.png">


## 스프링으로 변환하기

@Bean을 붙여 스프링 컨테이너에 스프링 빈으로 등록한다.

주석은 기존코드, 아래는 스프링 컨테이너

<img width="880" alt="10" src="https://user-images.githubusercontent.com/52316270/129543621-9c3b04d5-d3cb-4992-9a52-c6657561bd53.png">

<img width="496" alt="11" src="https://user-images.githubusercontent.com/52316270/129543639-802e258b-7c40-4cd3-bd07-d6b73892622f.png">

기존방식은 AppConfig를 만들고, 직접 생성하고 다하였지만

스프링에게 환경정보를 주고 찾을때는 스프링 컨테이너를 이용해 찾는 것

