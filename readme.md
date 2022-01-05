### 기술스택



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
    <p></p>
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
    <summary>ACID in DB</summary>
    <p>트랜잭션의 성질로 말함
    -> 
    <br>Atomicity(원자성) : 한 트랜잭션 내에서 실행한 작업들은 하나로 간주한다. 즉, 모두 성공 또는 모두 실패
    <br>Consistency(일관성) : 트랜잭션은 일관성 있는 데이터베이스 상태를 유지한다.
    <br>Isolation(격리성) : 동시에 실행되는 트랜잭션들이 서로 영향을 미치지 않도록 격리해야한다.
    <br>Durability(지속성) : 트랜잭션을 성공적으로 마치면 결과가 항상 저장되어야 한다. </p>
</details>











