### 책임 연쇄 패턴 (Chain of Responsibility Pattern)
- 책인 연쇄 패턴은 요청을 처리할 객체를 연결하여, 요청을 보내고 처리할 객체를 분리하는 디자인 패턴입니다. 
- 이 패턴을 통해 여러 객체가 요청을 처리할 수 있으며, 어떤 객체가 요청을 처리할지는 런타임에 결정됩니다.

### 사용 목적
- 요청을 여러 객체에 전달할 수 있게 하여 요청을 처리할 객체를 동적으로 변경할 수 있도록 함.
- 요청 처리의 유연성을 제공하고, 객체 간의 결합도를 낮춤.
- 특정 요청을 처리할 수 있는 객체를 명시적으로 지정할 필요가 없음.

### 사용 사례
- 이벤트 처리 시스템 (예: GUI에서 클릭 이벤트 처리).
- 로그 처리 시스템 (로그 레벨에 따라 다른 객체가 로그를 처리).
- 여러 단계의 승인 프로세스 (예: 구매 요청 승인).

### 구성 요소
- Handler: 요청을 처리하는 인터페이스 또는 추상 클래스. 다음 핸들러에 대한 참조를 유지.
- ConcreteHandler: 실제 요청을 처리하는 구체적인 클래스.
- Client: 요청을 보냅니다.

### 장단점
- 장점
  - 객체 간의 결합도를 낮춤.
  - 요청 처리의 유연성을 높임.
  - 새로운 핸들러를 추가하는 것이 용이함.
- 단점
  - 요청을 처리하지 않는 핸들러가 있을 경우 요청이 소실될 수 있음.
  - 전체 흐름을 추적하기 어려울 수 있음 (연쇄 구조로 인해).