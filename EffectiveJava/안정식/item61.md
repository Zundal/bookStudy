# 박싱된 기본 타입보다는 기본 타입을 사용하라  
1. 자바의 데이터 타입은 크게 2가지로 나뉜다
   1. 기본타입 
      1. int
      2. double
      3. boolean
   2. 참조타입 
      1. String
      2. List
   3. 박싱된 기본타입
      1. Integer
      2. Double
      3. Boolean

- 박싱과 오토 언박싱으로 기본 타입과 박싱된 기본타입은 크게 구분하지 않고 사용할 수 있다
- 박싱된 기본 타입과 기본타입의 차이점 
  1. 기본 타입은 값만 가지고 있다
     1. 박싱된 기본타입은 값에 더해 식별성 이란 속성을 갖는다 
     2. 박싱된 기본 타입의 두 인스턴스는 값이 같아도 서로 다르다고 식별 할 수 있다 
  2. 기본 타입의 값은 언제나 유효하다 
     1. 박싱된 기본 타입은 유효하지 않는 null을 가질 수 있다 
  3. 기본 타입이 박싱된 기본 타입보다 시간과 메모리 사용면에서 더 효율적이다 
```java
    new Interger(10) == new Interger(10) ... false 객체의 주소값이 달라서

    int x = 10;
    int y = 10;
    x == y ... true 기본값 int 10 의 값이 같아서
```


- 박싱된 기본타입은 언제 써야 하는가? 
  1. 컬렉션의 원소, 키, 값으로 쓴다 
     1. 컬렉션은 기본 타입을 감을 수 없으므로 어쩔 수 없이 박싱된 기본 타입을 써야만 한다 
```java
    ThreadLocal<int> ... X 잘못된 표현
    ThreadLocal<Integer> ... O 맞는 표현
```
요약 : 기본타입과 박싱된 기본 타입중ㅅ하나를 선택해야 할 때 가능하면 기본 타입을 사용하는게 더적은 오류와 더 빠를 속도의 프로그램을 개발할때 도움이 된다