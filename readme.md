### CS

<details>
    <summary>http 메소드</summary>
    <p>우리가 많이 알고있는 GET,POST,PUT,DELETE 뿐만아니라 HEAD, OPTIONS,TRACE,CONNECT가 있다.HEAD는 GET과 비슷하지만 웹서버에서의 헤더정보를 보낸다. OPTIONS는 시스템에서 지원되는 메소드 종류를 확인가능, TRACE는 루프백 메세지를 호출하기 위해 사용, CONNECT는 프락시 기능을 요청할때 사용. </p>
</details>

<details>
    <summary>http와 https</summary>
    <p>http는 hyper text transfer protocol으로 서버/클라이언트 모델을 따라 데이터를 주고 받기 위한 프로토콜이다. 즉, HTTP는 인터넷에서 하이퍼텍스트를 교환하기 위한 통신규약으로 80번 포트를 사용하고 있다. https는 http에 데이터 암호화가 추가된 프로토콜이다. HTTPS는 443번 포트를 사용한다. 중간에 제 3자가 정보를 볼 수 없도록 공개키 암호화를 지원하고 있다. <br>->그렇다면 https 동작과정은?<br>
    제3자 인증은 믿을 수 있는 인증기관에 등록된 인증서만 신뢰하는 것이고, 공개키 암호화는 비밀키를 공유하기 위해 사용합니다. 비밀키 암호화는 통신하는 데이터를 암호화하는데 사용합니다.<br>클라이언트는 TCP 3way handshake를 수행한 이후 Client Hello를 전송합니다. 서버는 인증서를 보냅니다.(다른 정보들도 전송하나 검색을 통해 알 수 있는 부분입니다. 대개 그 정도까지는 요구하지 않습니다.)<br>클라이언트는 받은 인증서를 신뢰하기 위해서 등록된 인증기관인지 확인합니다. 이 인증서는 인증기관의 개인키로 암호화되어있고, 공개키로 검증할 수 있습니다.(브라우저에 내장되어있음) 클라이언트는 사이트의 정보와, 서버의 공개키를 얻을 수 있습니다.<br>서버의 공개키로 통신에 사용할 비밀키를 암호화해서 서버에 보냅니다. 서버는 이를 개인키로 확인하고 이후 통신은 공유된 비밀키로 암호화되어 통신합니다.</p>
</details>

<details>
    <summary>process와 tread란?</summary>
    <p>프로세스는 운영체제로부터 자원을 할당받은 작업의 단위이고 스레드는 프로세스가 할당받은 자원을 활용하는 실행 흐름의 단위이다. 즉, 프로세스는 실행중인 프로그램을 의미한다. <br>->그렇다면 multi-thread란?<br>하나의 프로세스가 여러작업을 여러 스레드를 사용하여 동시에 처리하는 것을 의미한다.
    <br>->그렇다면 thread-safety란?<br>기본적으로 스레드는 스레드간 메모리를 공유하기 때문에, 하나의 스레드에서 문제가 생길경우 다른 스레드에 영향을 끼칠 수 있다. 그러한 부분에서 thread-safety란 여러 스레드가 사용되어도 안전하다는 것을 뜻한다.</p> 
</details>

<details>
    <summary>http의 request값들의 종류 </summary>
    <p>굉장히 많음....200(OK),400(사용자의 잘못된 요청을 처리할 수 없음), 401(Unauthorized),403(Forbidden 접근금지),404(요청한 페이지 없음) 등....</p>
</details>

<details>
    <summary>REST란?</summary>
    <p>HTTP URI를 통해 자원을 명시하고 HTTP메소드를 통해 해당 자원에 대한 CRUD를 적용하는 것을 의미한다. 또한,자원을 이름으로 구분하여 해당 자원의 상태를 주고 받는 모든 것을 의미한다. </p>
</details>

<details>
    <summary>CORS란?</summary>
    <p>Cross-Origin Resource Sharing의 줄임말로 보통 서로 다른 출처를 가진 리소르를 사용할 때 일어난다. 기본적으로 다른 출처인 리소스는 사용 불가능하기 때문에 해결방법은 "Access-Control-Allow-Origin" 헤더를 넣어주거나 프록시 기능을 이용해 CORS 정책을 우회하는 방법을 사용하는 것이 있습니다.</p>
</details>

<details>
    <summary>tcp와 udp의 차이점(+연결을 어떻게 보장하는지)</summary>
    <p>tcp는 연결 지향형 프로토콜이고 udp는 데이터를 데이터 그램 단위로 전송하는 프로토콜이다. tcp는 가상 회선을 만들어 신뢰성을 보장하도록하는 프로토콜이다. 따로 신뢰성을 보장하기 위한 절차가 없는 udp에 비해 속도가 느린편이다. 그래서 tcp는 파일전송과 같은 신뢰성이 중요한 서비스에 사용되고 udp는 스트리밍과 같이 연속성이 더 중요한 서비스에 사용된다. (+upd도 신뢰성을 udp자체에서 보장하지 않을 뿐, 개발자가 직접 설정가능)</p>
</details>

<details>
    <summary>ACID in DB</summary>
    <p>트랜잭션의 성질로 말함
    -> 
    <br>Atomicity(원자성) : 한 트랜잭션 내에서 실행한 작업들은 하나로 간주한다. 즉, 모두 성공 또는 모두 실패
    <br>Consistency(일관성) : 트랜잭션은 일관성 있는 데이터베이스 상태를 유지한다.
    <br>Isolation(격리성) : 동시에 실행되는 트랜잭션들이 서로 영향을 미치지 않도록 격리해야한다.
    <br>Durability(지속성) : 트랜잭션을 성공적으로 마치면 결과가 항상 저장되어야 한다. </p>
</details>




### 기술스택(자바,spring 관련)



<details>
    <summary>스프링과 Node.js의 차이점</summary>
    <p>보통 내가 스프링을 선택한 이유에서부터 이어지는 질문
    <br>->Spring은 thread가 여러개라 많은 요청을 동시에 처리가능하고 개발된지 오래되어서 버그나 보안문제에서도 안정성 높음.<br>노드는 한 개의 Thread로 수행하므로 효율적이고 빠른 개발이 가능하지만, 안정성 측면에서 떨어짐.</p>
</details>

<details>
    <summary>NosqlvsRDBMS</summary>
    <p>포토폴리오 관련 질문
    <br>-> RDMS : 정해진 규격,형식이 있는 데이터에 적합하고 데이터 간 관계가 있고 작업의 완전성을 보장함. <br>Nosql : 정해진 규격이 없으므로 데이터 저장이 자유롭고 확장성높음. 대부분 key-value 형식
   <br> -> NoSql들만의 공통점에 대한 질문받은 적있음.
    <br>-> 캐시...? 쪽으로 말씀해주셨던 것 같은데... 확실한 답안을 잘 모르겠다. Nosql에서 캐시라고 하면 보통 Redis인데.. 흠.. 아시는분 말씀좀..</p>
</details>
<details>
    <summary>JPA란</summary>
    <p>Java진영에서의 ORM(어플리케이션의 객체를 RDB테이블에 자동으로 영속화 해주는 것/내수준에선 쿼리가 아닌 코드로서 DB를 조작가능하게 하는 것)<br>->그렇다면 JPA를 사용하는 이유는?<br>JPA를 사용하는 이유는 객체지향 프레임워크로서 비지니스 로직이 RDBMS에 의존하는 것이 아니라, 자바 코드로 표현될 수 있어 생산성이 높아지기 때문입니다.<br>->N+1문제가 발생하는 이유와 이를 해결하는 방법은?<br>1개의 쿼리를 실행했을 때, 내부에 존재하는 컬렉션들을 조회해오면서 생기는 문제입니다. OnetoMany 어노테이션 매핑을 하지 않거나 사용할경우, Fetch Join 과 EntityGraph를 사용하는 방법이 있습니다. </p>
</details>


<details>
    <summary>DAO 와 DTO</summary>
    <p></p>
</details>

<details>
    <summary>JDBC를 할 때 필요한 것</summary>
    <p>데베와 연결 경험에서부터 질문받은것 -> mapper</p>
</details>

<details>
    <summary>spring에서의 트랜젝션이란</summary>
    <p>작업의 완전성,무결성을 보장해주는 것으로 작업 중 문제가 발생할 경우, 원상태로 복구해 작업의 일부만 적용되는 현상이 발생하지 않게 만들어주는 기능
    <br>-> 이 질문에서 내가 정의는 잘 모르지만, 개발중 트랜젝션 어노테이션을 통해 문제가 생길 경우, 다시 돌아가게 할 때 사용했다라고 대답하자 그렇다면 롤백은 무엇인가? 라는 질문들어옴
    <br>-> 아마 트랜젝션과 롤백의 차이점을 물어보신듯
    <br>-> 롤백이란?
    <br>-> 롤백은 데이터변경사항이 취소되어 데이터 이전상태로 복구되는 것이며 트랜젝션은 변경된 데이터를 영구적으로 반영하는 커밋,다시 돌아가는 롤백,일부 롤백하는 저장점의 선택지 3개를 통해 작업의 완전성을 보장해주는것</p>
</details>
<details>
    <summary>exception의 종류 2가지(자바)</summary>
    <p>Checked Exception과 Unchecked Exception가 있으며, 전자(일반예외)는 개발자가 반드시 예외처리를 직접 진행해야하는 것이고 후자(실행예외)는 개발자가 직접하지 않아도 된다. </p>
</details>

<details>
    <summary>Map, Hash설명</summary>
    <p>key와 value로 구성된 컬렉션</p>
</details>


<details>
    <summary>자바 특징</summary>
    <p><br>->자바와 C++의 차이점
    <br>->자바가 왜 람다식을 지원하게 되었을까?
    <br>->자바의 GC에 대해 설명
    <br>->자바 전체 구조 다 설명</p>
</details>
<details>
    <summary>abstract와 interface의 차이점</summary>
    <p>추상클래스는 객체의 추상적인 상위개념으로 공통된 개념을 표현할 때 사용하나 인터페이스는 구현 객체가 같은 동작을 한다는 것을 보장하기 위해 사용한다. 전자는 단일상속만 가능하고 연관관계가 있지만, 후자는 다중상속이 가능하고 관계가 없을 수 있다.</p>
</details>

<details>
    <summary>오버로드, 오버라이딩의 차이점</summary>
    <p>오버로드는 자바의 한 클래스 내에 이미 사용하려는 이름과 같은 이름을 가진 메소드가 있더라도 매개변수의 개수 또는 타입이 다르면, 같은 이름을 사용해서 메소드를 정의할 수 있는 것. 오버라이드는 부모클래스로부터 상속받은 메소드를 자식 클래스에서 재정의 하는 것이므로 메소드의 이름, 매개변수, 리턴값이 모두 같아야함.<br>->final을 쓰면 오버로드, 오버라이드의 차이점<br>오버라이딩에서 final을 쓸경우 더이상 오버라이딩 불가. 하지만 오버로드는 메서드 이름만 똑같을 뿐 다르므로 final과 상관없다</p>
</details>

<details>
    <summary>stringbuilder과 stringbuffer의 차이점</summary>
    <p>StringBuilder와 StringBuffer는 Thread-safe 여부의 차이가 있다. StringBuilder는 Thread-safe하지 않다. 그래서 멀티스레드 환경에서 사용할 때는 StringBuffer를 사용한다.</p>
</details>


<details>
    <summary>java 자료구조 종류</summary>
    <p></p>
</details>




