### CS

<details>
    <summary>http 메소드</summary>
    <p>우리가 많이 알고있는 GET,POST,PUT,DELETE 뿐만아니라 HEAD, OPTIONS,TRACE,CONNECT가 있다.HEAD는 GET과 비슷하지만 웹서버에서의 헤더정보를 보낸다. OPTIONS는 시스템에서 지원되는 메소드 종류를 확인가능, TRACE는 루프백 메세지를 호출하기 위해 사용, CONNECT는 프락시 기능을 요청할때 사용. <br>->그렇다면 루프백과 프록시에 대해 간단히 설명하시오<br><br>->그렇다면 GET과 POST의 차이점은?<br>get은 캐시가 가능하고 히스토리에 남으며 길이제한이 있으나 post는 캐시되지 안ㅇㅎ으며 히스토리에 남지 않고 길이제한이 없다. post는 body에 정보를 보냄<br>캐시란 데이터나 값을 미리 복사해 놓는 임시장소를 가리킴</p>
</details>

<details>
    <summary>http와 https</summary>
    <p>http는 hyper text transfer protocol으로 서버/클라이언트 모델을 따라 데이터를 주고 받기 위한 프로토콜이다. 즉, HTTP는 인터넷에서 하이퍼텍스트를 교환하기 위한 통신규약으로 80번 포트를 사용하고 있다. https는 http에 데이터 암호화가 추가된 프로토콜이다. HTTPS는 443번 포트를 사용한다. 중간에 제 3자가 정보를 볼 수 없도록 공개키 암호화를 지원하고 있다. <br>->그렇다면 https 동작과정은?<br>
    제3자 인증은 믿을 수 있는 인증기관에 등록된 인증서만 신뢰하는 것이고, 공개키 암호화는 비밀키를 공유하기 위해 사용합니다. 비밀키 암호화는 통신하는 데이터를 암호화하는데 사용합니다.<br>클라이언트는 TCP 3way handshake를 수행한 이후 Client Hello를 전송합니다. 서버는 인증서를 보냅니다.(다른 정보들도 전송하나 검색을 통해 알 수 있는 부분입니다. 대개 그 정도까지는 요구하지 않습니다.)<br>클라이언트는 받은 인증서를 신뢰하기 위해서 등록된 인증기관인지 확인합니다. 이 인증서는 인증기관의 개인키로 암호화되어있고, 공개키로 검증할 수 있습니다.(브라우저에 내장되어있음) 클라이언트는 사이트의 정보와, 서버의 공개키를 얻을 수 있습니다.<br>서버의 공개키로 통신에 사용할 비밀키를 암호화해서 서버에 보냅니다. 서버는 이를 개인키로 확인하고 이후 통신은 공유된 비밀키로 암호화되어 통신합니다.</p>
</details>

<details>
    <summary>process와 tread란?</summary>
    <p>프로세스는 운영체제로부터 자원을 할당받은 작업의 단위이고 스레드는 프로세스가 할당받은 자원을 활용하는 실행 흐름의 단위이다. 즉, 프로세스는 실행중인 프로그램을 의미한다.스레드는 실행 제어만 분리한 것을 의미한다. <br>->그렇다면 스레드가 필요한 이유는? <br>Context_Switching할 때 공유하고 있는 메모리만큼의 메모리 자원을 아낄 수 있으며 스레드는 프로세스 내의 스택 영역을 제외한 모든 메모리를 공유하기 때문에 통신의 부담이 적어서 응답 시간이 빠르다.<br>->그렇다면 multi-thread란?<br>하나의 프로세스가 여러작업을 여러 스레드를 사용하여 동시에 처리하는 것을 의미한다.
    <br>->그렇다면 thread-safety란?<br>기본적으로 스레드는 스레드간 메모리를 공유하기 때문에, 하나의 스레드에서 문제가 생길경우 다른 스레드에 영향을 끼칠 수 있다. 그러한 부분에서 thread-safety란 여러 스레드가 사용되어도 안전하다는 것을 뜻한다.</p> 
</details>

<details>
    <summary>context-switching이란?</summary>
    <p>한 Task가 끝날 때까지 기다리는 것이 아닌 여러 작업을 번갈아가며 실행해서 동시에 처리될 수 있도록 하는 방법이다.  </p>
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
    <p>Cross-Origin Resource Sharing의 줄임말로 보통 서로 다른 출처를 가진 리소스를 사용할 때 일어난다. 기본적으로 다른 출처인 리소스는 사용 불가능하기 때문에 해결방법은 "Access-Control-Allow-Origin" 헤더를 넣어주거나 프록시 기능을 이용해 CORS 정책을 우회하는 방법을 사용하는 것이 있습니다.</p>
</details>

<details>
    <summary>tcp와 udp의 차이점(+연결을 어떻게 보장하는지)</summary>
    <p>tcp는 연결 지향형 프로토콜이고 udp는 데이터를 데이터 그램 단위로 전송하는 프로토콜이다. tcp는 가상 회선을 만들어 신뢰성을 보장하도록하는 프로토콜이다. 따로 신뢰성을 보장하기 위한 절차가 없는 udp에 비해 속도가 느린편이다. 그래서 tcp는 파일전송과 같은 신뢰성이 중요한 서비스에 사용되고 udp는 스트리밍과 같이 연속성이 더 중요한 서비스에 사용된다. (+upd도 신뢰성을 udp자체에서 보장하지 않을 뿐, 개발자가 직접 설정가능)</p>
</details>

<details>
    <summary>TCP 3-way Handshake, TCP 4-way Handshake란?</summary>
    <p>TCP 3-way Handshake : 정확한 전송을 보장하기 위해 상대방 컴퓨터와 사전에 세션을 수립하는 과정을 의미한다.TCP 4-way Handshake : 전자가 TCP의 연결을 초기화 할때 사용한다면, 이것은 세션을 종료하기 위해 수행되는 절차입니다. <br>->각각의 과정은? </p>
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

<details>
    <summary>OSI7계층</summary>
    <p>네트워크 통신을 구성하는 요소들을 7개의 계층으로 표준화한것<br>물리계층
    <br>데이터 링크 계층<br>네트워크 계층<br>전송계층<br>세션 계층<br>표현계층<br>응용계층</p>
</details>

<details>
    <summary>쿠키와 세션의 차이점</summary>
    <p>기본적으로 둘은 정보(로그인 정보)를 저장한다. BUT, 쿠키는 로컬에 저장, 세션은 서버에 저장
    <br></p>
</details>

<details>
    <summary>블로킹과 논블로킹이란?</summary>
    <p>자신의 작업을 하다가 다른 작업 주체가 하는 작업의 시작부터 끝까지 기다렸다가 다시 자신의 작업을 시작한다면 이는 블로킹이고, 다른 주체의 작업과 관계없이 자신의 작업을 계속한다면 이를 논블로킹이라고 한다. (ex.블로킹=JDBC를 사용해 DB에 질의를 날리고 해당 결과를 받아오는 작업)<br>->그렇다면 비동기 동기와는 어떤점이 다른가?<br>비동기/동기는 작업을 수행하는 주체에 기준을, 블로킹/논블로킹은 작업을 수행하는 주체에 초점을 맞춤
    <br></p>
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
    <br>함수형 프로그래밍을 지원하기위해. 
    <br>->자바의 GC에 대해 설명
    <br>힙 영역에서 사용하지 않는 객체들을 제거하는 작업을 총칭한다.
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
<details>
    <summary>객체지향 프로그래밍 5가지</summary>
    <p><br>클래스+인스턴스(객체)<br>클래스:집단에 속하는 속성과 행위를 변수와 메서드로 정의한것,객체:클래스에서 정의한 것을 토대로 실제 메모리에 할당된 것
    <br>추상화<br>공통의 속성이나 기능을 묶어 이름을 붙이는 것
    <br>캡슐화<br>기능과 특성의 모음을 클래스라는 캡슐에 분류해서 넣는 것
    <br>상속<br>부모클래스의 속성과 기능을 그대로 이어받아 사용할수 있게 하는것
    <br>다형성<br>하나의 변수명, 함수명 등이 상황에 따라 다른 의미로 해석될 수 있는 것(ex.오버라이딩, 오버로딩)</p>
</details>

<details>
    <summary>java 자료구조 종류</summary>
    <p></p>
</details>



### 포토폴리오 관련(포토폴리오 관련 지식 질문X)

<details>
    <summary>EcoDiary에서 마지막 부분에 객체지향적인 코드가 무엇인지 계속 생각했다고 했는데 객체지향적인 코드란 무엇인가요?</summary>
    <p>코드 재사용이 용이하고 유지보수가 쉬운 코드라고 생각하고 개발했으며 작게는 하나의 함수에 하나의 기능을 하게 하거나 크게는 JPA를 사용하는 것이 이에 해당합니다.<br>->JPA가 왜 객체지향일까요?<br>JPA를 사용하지 않을 경우, mapper를 사용해서 쿼리에 집중하게 됩니다. 그렇게 되면, 객체를 데이터 전달 역할로서 주로 사용하게 됩니다. 하지만 JPA를 사용하면, 객체와 테이블을 매핑함으로써 기본제공CRUD쿼리를 바탕으로 객체에 중심을 쏟을 수 있게 됩니다. </p>
</details>

<details>
    <summary>객제치향형과 절차지향형의 차이</summary>
    <p>절차지향은 말그대로 순서대로 코드를 작성하는 기법으로 코드의 순서가 바뀌면 동일한 결과를 보장하기 어렵고 유지보수가 어려우나 실행속도가 빠릅니다. 객체지향은 컴퓨터 부품을 하나씩 사 조립을 하는 것과 같이 하나하나의 기능에 따라 코딩을 작성하는 기법입니다. 그렇기 때문에 코드의 재활용성이 높습니다만 그만큼 처리속도가 느립니다.</p>
</details>

<details>
    <summary>EcoDiary 프로젝트에서 가장 힘들었거나 고민을 많이 한 부분은 어디일까요?그리고 그 부분을 어떤식으로 해결했을까요?</summary>
    <p>많은 부분을 고민하고 해결했지만, 아무래도 처음 개발을 시작할때부터 고민이 들었던 패키지 구조가 기억에 남습니다. 처음에는 패키지 구조에 대해 정답을 찾으려고 했지만, 구조마다 각자의 장단점이 있기때문에 사람들마다의 구조는 매우 다양했습니다. 작은 프로젝트를 하는 저로서는 도메인형이 더 깔끔하다고 느꼈고 그렇게 진행했지만, 규모가 커질수록 패키지간의 참조가 많아져 결국에는 계층형이 맞지 않을까 하는 생각이 들었습니다. 그래서 끝난후, 패키지 구조에 정답은 없으며 그때그때마다 맞는 구조를 적용해야한다는 것을 깨달았습니다.  </p>
</details>

<details>
    <summary>여러 분야의 지식이 실제 개발에 쓰이면서 서버개발의 매력을 알게되었다고 하셨는데 어떤 예가 있을까요?</summary>
    <p>처음에 서버를 시작하고 API를 만들게 되면서 URI를 작성하게 되었습니다. URI를 작성하며 평소에 내가 봤던 주소들이 저런 의미였구나를 알게되고 내가 현재 어떤 포트를 사용하고, 어떤 프로토콜이고 사용자는 누구인지 등에 대해 평소 스쳐지나갔던 CS지식들이 눈 앞에 바로 사용되고 있었구나를 실감하게 되었습니다. 
    <br></p>
</details>

<details>
    <summary>URI법칙?</summary>
    <p>/후행슬래시는 URI에 포함되지 않아야한다.<br>계층관계를 나타낼때 슬래시 구분자를 사용해야한다.<br>URI의 가독성을 높이기 위해서 하이픈 문자를 사용한다. <br> 언더바 문자는 URI에 사용하지 않는다. <br>URI를 작성하는 데에는 소문자가 적합하다. <br> 파일확장자는 URI에 포함하지 않습니다. <br> </p>
</details>







