# os-deep-dive
#### 운영체제(Operating System)와 정보기술, 컴퓨터 구조와 프로그래밍에 대한 키워드 중심의 정리 글. 관련 서적들의 내용을 발췌하여 정리하였으며 출처는 하단에 명시하였음.

<details>
<summary>핵심은 변하지 않는다</summary>

하드웨어는 급속도로 발전하고 소프트웨어도 새로운 버전이 등장하지만 컴퓨터 분야의 기본 원리와 정보기술이 추구하는 핵심 철학은 시대가 흘러도 변하지 않는다.

1937년의 수학자 앨런튜링이 개발한 이록적 컴퓨터가 현대 최첨단 컴퓨터가 풀 수 있는 모든 문제를 풀 수 있다는 사실이 증명되었다.

연역법은 컴퓨터의 이론적 기원이다.
</details>

<details>
<summary>운영체제가 없다면?</summary>

모든 애플리케이션 개발자가 하드웨어의 스펙을 상세히 알아야만 조작할 수 있다. 멀티 프로세스가 동시에 디바이스를 조작할 경우 예상 외의 동작이 발생할 수 있다. 이러한 이유들로 개발 비용이 매우 커진다.

</details>

<details>
<summary>왜 하부 기술을 이해해야 하는가</summary>

자바는 부분적으로는 당시 널리 쓰이던 C 프로그래밍 언어를 본떠 만들어졌다. C에는 메모리 자동 관리가 없었고, 메모리 관리 오류는 당시 프로그래머에게 자주 두통을 일으키게 하는 오류였다. 자바는 언어 설계를 통해 메모리 관련 오류를 없앴다. 자바는 메모리 관리를 프로그래머가 볼 수 없게 감춤으로써 초보자에게 좋은 언어가 되었다.

하지만 좋은 프로그래머와 좋은 프로그램을 탄생시키려면 좋은 프로그래밍 언어 이상의 것이 필요하다. 자바로 인해, 디버깅하기 더 어려운 새로운 버그 종류가 생겨났음이 드러났다.

처음 시작하는 프로그래머들에게는 안전한 프로그래밍 환경이 덜 두려울 테지만, 나중에 만나게 될 실제 세계를 미리 대비할 필요가 있다.

요즘은 더 이상 프로그램을 작성하기 위해 여러 해 동안 연습을 하거나 이론을 배우지 않는다. 그렇다고 해서 이런 식으로 작성된 프로그램이 좋은 프로그램이거나 신뢰할 만한 프로그램인 것은 아니다. 누구나 프로그래머가 되도록 만드는 운동의 목표는 훌륭한 프로그래머를 낳는 게 아니라 질 낮은 프로그래머를 회사에 많이 공급함으로써 프로그래머의 급여 수준을 낮추고 이를 통해 소프트웨어 회사의 이익을 증가시키는 것이다.

하부 기술을 잘 이해하면 무엇이 잘못되고 있는지 알아차리는 능력을 계발할 수 있다. 고수준 도구만 알면 잘못된 질문을 던지기 쉽다. 하부 기술을 이해하면 새로운 도구를 만들어낼 수도 있다.

만약 응용 프로그래머로 일하고 싶다면 시스템 프로그래밍을 배우지 않아도 된다. 하지만 시스템 프로그래밍을 배우지 않는다면 도메인을 벗어나는 문제가 생기면 문제를 직접 해결하려고 파고들기보다는 도움을 줄 수 있는 사람을 찾는 편이 더 낫다.

</details>

<details>
<summary>인코딩</summary>

* ASCII Code : 정보 교환을 위한 미국 표준 코드, 키보드에 있는 모든 기호에 대해 7비트 수 값을 할당 함. 영어를 표현하며, 제어 문자가 포함되어 있다.
* UNI Code : 전 세계의 모든 문자를 다루도록 설계된 표준 문사 전산 처리 방식
* UTF-8(Unicode Transformation Format-8 bit) : ASCII와 Unicode를 호환하는 규격, UTF-8은 모든 아스키 문자를 8비트로 표헌하기 때문에 아스키 데이터를 인코딩 할 때 추가 공간을 필요로 하지 않는다.
* Base64 : 아스키 코드 중 상당수가 제어 문자로 예약되어 있고 제어 문자는 시스템에 따라 처리하는 방식이 달라 전송이 어려워 만들어진 인코딩 방식
* URL 인코딩 : 퍼센트 인코딩이라고도 불리며 % 뒤에 어떤 문자의 16진 표현을 덧붙이는 방식으로 문자를 인코딩
* 색 인코딩 : 16진 트리플렛(hex triplet)을 이용해 인코딩 한다. #ffff00 의 예시.

</details>

<details>
<summary>컴퓨터와 프로그래밍의 역사</summary>

* 이론적 컴퓨터 - 앨런 튜링(1930년대)
* 기계식 컴퓨터
  * 찰스 배비지
  * 1823년 반복적인 연산을 수행하는 미분기계
  * 19세기 해석기관(천공카드로 20자리까지의 연산을 수행하며 입출력, 처리, 저장 장치를 포함)
* 전자식 컴퓨터
  * 1943년 콜로서스(군사용 암호를 해독하기 위한 컴퓨터)
  * 1944년 Mark I(둘레 16미터, 높이 2.5미터지만 현대의 휴대용 전자계산기보다 느림)
  * ENIAC(18,000여 개의 진공관, 무게 30톤, 7분에 한 번씩 오류, 현대의 휴대용 전자계산기 정도)
    * 최초의 현대식 컴퓨터로 인식
* 근대적 컴퓨터
  * 1세대 컴퓨터 : 진공관 기반(1940년대)
  * 2세대 컴퓨터 : 트랜지스터 기반(1950년대)
  * 3세대 컴퓨터 : 집적회로 기반(1960년대)
  * 4세대 컴퓨터 : 고밀도 집적회로 기반(1970년대)

컴퓨터의 사용이 확산됨에 따라 프로그래밍이 필요해졌다. 기계어의 불편함 때문에 어셈블리어(1950년대 후반)가 등장했고, 문제 자체에 더 가까운 언어가 필요하다고 생각되어 고급 언어인 포트란이 생겼다.

1960년대에는 소프트웨어의 규모가 커짐에따라 인간이 이해하기 쉬운 작은 단위들로 나누어 각 단위를 독립적으로 프로그래밍 하는 **구조적 프로그래밍**이 기법이 대두되었다.
이 시기에 운영체제가 개발되었다. 초창기에는 하드웨어 자체를 관리하는 일과 프로그램을 작성하는 일을 사용자가 다 해야했다. 초기에는 컴퓨터 외부에서 미리 예약하는 일괄처리 방식을 사용하다가, 컴퓨터가 자동으로 처리해주도록 하는 방식을 고민한 결과 운영체제가 탄생했다. 은행 업무 전산화를 위해 DBMS가 등장했다.

1970년대 이후 하드웨어의 발전으로 PC가 등장하고, C 언어(1972년)가 개발되었다.

1980년대 이후에는 프로그래밍적으로 고품질 소프트웨어를 개발하는 도구로써의 객체지향 언어가 성공했다.

1990년대  초반부터는 윈도우, 월드와이드웹(WWW), Java가 출연했다.
</details>

<details>
<summary>하드웨어의 크기</summary>

오늘날 컴퓨터 클록 속도는 4GHz이며, 1초에 40억 가지 계산을 처리할 수 있는데 40억 분의 1초 동안 전자가 이동할 수 있는 거리는 75밀리미터뿐이다. CPU의 한 면이 18밀리미터라고 한다면 40억 분의 1초는 전자가 이 CPU를 고작 두 번 왕복할 수 있는 정도의 시간이다. 따라서 컴퓨터에서 모든 것을 작게 만들면 더 높은 성능을 달성할 수 있음이 분명해보인다.

하지만 물체가 너무 작아지면 서로 간섭하기 아주 쉬워지는데, 현대 컴퓨터 칩 안의 선은 서로 몇 나노미터 떨어져 있기 때문에 높은 판정 기준과 안정성이 필요하다.

</details>

<details>
<summary>오버플로</summary>

연산 결과가 사용할 비트의 개수로 표현할 수 있는 범위를 벗어났을 때 오버플로가 발생했다고 한다. 오버플로란 말은 MSB(Most Significant Bit)에서 올림이 발생했다는 뜻이다.

</details>

<details>
<summary>비트 그룹의 이름</summary>

컴퓨터를 설계하는 사람은 비용을 고려해 컴퓨터가 사용할 비트의 개수와 비트들의 조직을 결정해야 한다. 시간이 지남에 따라 세계적으로 8비트 덩어리가 기본단위로 널리 쓰이기 시작했고 이를 바이트(Byte)라고 부른다.

다른 크기의 덩어리들도 가리키기 쉽도록 이름이 붙어있는데 니블(nibble - 4bit), 하프 워드(half word - 16bit), 워드(word - 32bit) 등이 있다. 여기서 워드는 각 컴퓨터가 설계상 자연스럽게 사용할 수 있는 비트 묶음의 크기를 가리키는 말로 쓰인다. 자연스럽게 쓸 수 있다는 말은 컴퓨터가 가장 빠르게 처리할 수 있는 가장 큰 덩어리를 뜻하며, 컴퓨터 마다 다르다.

</details>


<details>
<summary>운영체제란</summary>

운영체제는 컴퓨터 하드웨어 바로 윗단에 설치되는 소프트웨어를 말한다. 컴퓨터의 전원을 켜면 운영체제는 이와 동시에 실행된다. 소프트웨어는 실행되기 위해 메모리에 프로그램이 올라가있어야 하는데, 운영체제 자체도 하나의 소프트웨어로서 전원과 동시에 메모리에 올라간다. 하지만,
운영체제와 같이 큰 규모의 프로그램이 모두 메모리에 올라가면 낭비가 심하여 항상 필요한 부분만이 메모리에 올라가는데, 상주하는 운영체제의 부분을 **커널** 이라고 하고 이를 좁은 의미의 운영체제라고도 한다.

운영체제는 하드웨어를 위한 역할과 사용자를 위한 역할을 수행한다. 컴퓨터 시스템 내의 자원을 효율적으로 관리하고 사용자가 사용할 수 있는 환경을 제공하는 것이다.
</details>

<details>
<summary>CPU와 메모리는 공유된다</summary>

CPU가 하나라여서 매 순간 하나의 프로그램만 CPU에서 실행되더라도 짧은 시간의 규모로 여러 프로그램들이 CPU에서 번갈아 실행되고 이를 시분할 시스템이라고 부른다.

메모리는 여러 프로그램이 조금씩 메모리 공간을 보유하며 동시에 메모리에 올라갈 수 있다. 이를 다중 프로그래밍 시스템이라고 부른다.
</details>

<details>

<details>
<summary>ROM</summary>

Read-Only Memory 라는 이름은 그리 정확한 이름은 아니다. ROM은 한 번 쓰고 나면 여러 번 읽을 수 있어, 전자레인지 같이 프로그램을 내장해야 하는 장치에서 유용하다.

</details>

<details>
<summary>SSD</summary>

고체 상태 드라이브(Solid-State Drive)는 디스크 드라이브 모양의 패키지에 넣은 플래시 메모리와 같다. 플래시 메모리는 점차 낡지만 SSD에는 여러 블록의 쓴 횟수를 기억해서 모든 블록이 가능하면 똑같은 수준으로 낡도록 조정하는 포러세서가 들어 있다.

</details>

<details>
<summary>산술 논리 장치(ALU)</summary>

산술 논리 장치(ALU)는 CPU의 핵심 부품이다. ALU는 산술 계산, 불리언 대수 및 기타 연산을 수행하는 방법을 알고 있는 장치이다. 명령코드, 피연산자, 결과, 조건 코드 등으로 조작된다.

</details>

<details>
<summary>메모리 계층</summary>

현대 컴퓨터에는 수백 개의 레지스터가 있지만, 전체 메모리에서 차지하는 비율은 작다. 프로세서는 보통 RAM으로 이루어진 주 메모리와 통신하는데, 주 메모리는 프로세서보다 1/10의 속도밖에 되지 않는다. 디스크 드라이브 등의 저장장치는 프로세서보다 백만 배 느릴 수도 있다. 그렇다면, CPU가 메모리를 기다리느라 많은 시간을 소비해야 하는데, 이를 해결하기 위해 캐시(cache)라는 하드웨어를 CPU에 추가한다.

CPU - 레지스터 - L1캐시 - L2캐시 - L3 캐시 - 주 메모리 - 대량 저장장치의 순서로 메모리 계층을 가진다.

</details>

<summary>자원 관리</summary>

하드웨어 자원은 CPU와 메모리를 비롯해 주변장치(입출력 장치)들로 구성된다. CPU와 메모리는 전원이 꺼지면 모두 지워지기 때문에 기억해야 하는 부분을 IO Device 중 하나인 보조기억장치에 파일 형태로 저장한다.

CPU는 여러 프로세스가 동시에 수행될 수 있으므로 효율적이고 공평하게, 특정 프로세스가 불이익을 당하지 않도록 관리한다. FCFS, Round Robin, Priority 등의 방법이 있다.

메모리는 CPU가 직접 접근할 수 있는 컴퓨터 내부의 기억장치인데, 메모리의 어느 부분이 어떤 프로그램에 의해 사용되는지 파악해서 유지하는데 필요한 정보를 주소라고 부른다. 메모리 내부 위치는 행과 열을 조합해 지정된다. 메모리 관리 기법은 고정분할, 가변분할, 가상메모리 방식이 있다. 특히 가상메모리 방식은 가장 널리 사용되는 메모리 관리 기법인데, 물리 메모리 주소와 매핑하여 사용하는 방식을 사용한다.
현재 사용되고 있는 부분만 메모리에 올리고, 나머지는 하드디스크와 같은 보조기억 장치에 저장해두었다가 필요할 때 적재하는데 이때 보조장치의 영역을 **스왑 영역** 이라 한다.
</details>

<details>
<summary>로컬버퍼</summary>

입출력 장치의 컨트롤러는 장치로부터 오고 나가는 데이터를 임시로 저장하기 위한 작은 메모리를 가지고 있는데 이것이 로컬버퍼다. 디스크나 키보드 등에서 데이터를 읽어올 때 로컬버퍼에 데이터가 임시로 저장된 후 메모리에 전달된다. 장치에서 로컬버퍼로 읽어오는 일은 컨트롤러가 담당한다.

**프로그램 실행 중 디스크에서 데이터 읽기 명령 > 디스크 컨트롤러가 물리 영역에서 읽어 로컬버퍼 저장 > 완료 시 컨트롤러가 인터럽트를 발생시켜 보고 > CPU 옆 인터럽트 라인에 신호 발생 > CPU가 먼저 처리**
</details>

<details>
<summary>인터럽트</summary>

A라는 프로그램이 CPU를 할당받고 명령을 수행하는 도중 인터럽트가 발생하면 A는 현재 수행 중인 명령의 위치를 저장하고 운영체제 내부 코드인 인터럽트 처리루틴으로 넘어가서 인터럽트 처리를 하고 다시 돌아와 A의 이전 작업 지점부터 수행을 계속 이어간다. 필요한 복귀 주소는 Stack 영역에 보관한다.

CPU에서 명령이 실행될 때는 CPU 내부의 임시 기억장치인 레지스터에 데이터를 읽거나 쓰는데, 이때 인터럽트로 새로운 명령을 실행하면 기존값이 지워지기 때문에 PCB 자료구조를 둔다. 구체적으로는 실행 중이던 코드의 메모리 주소와 레지스터값, 하드웨어 상태 등을 저장한다. 즉 인터럽트 때문에 CPU를 빼앗긴 위치는 운영체제가 관리하는 프로세스 제어블록(PCB)에 저장된다.

인터럽트 발생 시 해주어야 할 작업을 정의한 프로그램 코드인 인터럽트 코드는 운영체제마다 다르다. 주변 장치들은 장치를 관리하기 위해(그 중 하나로 인터럽트를 발생시키기 위해) 작은 CPU를 가지고 있고 이를 컨트롤러라고 부른다.
컨트롤러가 CPU에게 인터럽트를 알리면 CPU는 현재 수행중인 작업을 저장하고 운영체제 내의 키보드 인터럽트 처리루틴을 찾아간다. 처리루틴은 입력받은 내용을 메모리의 특정 부분에 저장하고 해당 프로그램의 입력을 알리면서 인터럽트를 완료한다.

</details>

<details>
<summary>소프트웨어 인터럽트</summary>

트랩(trap)이라는 용어로 불리는 소프트웨어 인터럽트는 예외상황(Exception)과 시스템 콜(System Call)이 있다. 예외상황은 흔히 프로그래밍 언어에서 Exception 이 터졌을 때 처리를 위해 발생시키는 인터럽트이고, 시스템 콜은 프로그램이 운영체제 내부에 정의된 코드를 실행하고 싶을 때 운영체제에 서비스를 요청하는 방법이다. 예를 들어 개발자가 개발 중 I/O 작업이 필요할 경우 직접 입출력을 수행하는 코드를 작성하는 것이 아니라 존재하는 커널의 코드를 호출하는 것이다.

</details>

<details>
<summary>시스템 콜 Wrapper</summary>

시스템 콜은 보통의 함수 호출과는 다르게 C 언어 등의 고급 언어에서는 직접 호출이 불가능하다. 아키텍처에 의존하는 어셈블리 코드를 사용해 호출할 필요가 있다. 만약 OS의 도움이 없다면 각 프로그램은 시스템 콜을 호출할 때마다 아키텍처에 의존하는 어셈블리 언어를 써서 고급언어로부터 어셈블리 코드를 호출해야만 했을 것이다.

이러한 문제를 해결하기 위해서 OS는 내부적으로 시스템 콜을 호출하는 일만 하는 함수를 제공하는데 이를 시스템 콜 wrapper 라고 한다. wrapper 함수는 아키텍처별로 존재하며, 고급언어로 써진 사용자 프로그램에서는 각 언어에 대응하여 준비된 시스템 콜의 wrapper 함수를 호출하기만 하면 된다.

</details>

<details>
<summary>starce 명령어</summary>

리눅스 시스템에서는 strace 명령어를 통해 시스템 콜 호출을 추적할 수 있다. 각각 C언어와 파이썬으로 작성한 프린트 코드를 strace로 추적해보면 결국 write() 시스템 콜이 호출된다. 이는 다른 복잡한 프로그램에도 모두 해당된다.

strace에 -T 옵션을 붙이면 시스템 콜 처리에 걸린 시간을 마이크로초 단위로 정밀하게 측정할 수 있다.

</details>

<details>
<summary>폴링(Polling)</summary>

프로그램이 충돌 회피 또는 동기화 처리 등을 목적으로 다른 장치의 상태를 주기적으로 검사하여 일정한 조건을 만족할 때 처리하는 방식

</details>

<details>
<summary>DMA(Direct Memory Access)</summary>

원칙적으로 메모리는 CPU에 의해서만 접근할 수 있는 장치이지만, 컨트롤러가 CPU에게 인터럽트를 발생시키고, CPU는 컨트롤러의 로컬버퍼와 메모리 사이에서 데이터를 옮기는 일을 하게 된다. 하지만 모든 메모리 접근이 CPU에 의해서만 이루어질 경우
모든 I/O가 CPU의 업무를 방해하므로 효율이 떨어진다. 이를 위해 CPU 이외에 메모리 접근이 가능한 장치를 하나 더 두는데 이를 DMA 라고 한다.

DMA를 사용하면 로컬버퍼에서 메모리로 읽어오는 작업을 CPU가 담당하는 것이 아니라 DMA가 대행함으로써 CPU의 비효율을 줄인다. DMA는 바이트 단위가 아니라 블록이라는 큰 단위로 정보를 메모리로 읽어온 후 CPU에게 인터럽트를 발생시켜 해당 작업의 완료를 알린다.

</details>

<details>
<summary>저장장치의 구조</summary>

컴퓨터 시스템을 구성하는 저장장치는 휘발성인 주기억장치 메모리(RAM), 비휘발성인 보조기억장치가 있다.

보조기억장치는 파일 시스템과 스왑 영역을 위해 활용된다.메모리는 크기가 한정되고 비싸서 쉽게 부족한데, 당장 필요한 부분만 메모리에 올리고 그렇지 않은 부분은 디스크의 스왑 영역에 내려놓는다. 이를 스왑 아웃(swap out) 시킨다고 말하며, 다시 필요할 때 메모리 영역으로 올린다.

</details>

<details>
<summary>커널 모드와 사용자 모드</summary>

커널모드는 운영체제가 CPU의 제어권을 가지고 운영체제 코드를 실행하는 모드로, 모든 종류의 명령을 다 실행할 수 있다.

사용자모드는 일반 사용자 프로그램을 실행하며 제한적인 명령만을 수행한다. 특히 디바이스 조작, 프로세스 관리 시스템, 프로세스 스케줄링, 메모리 관리 시스템, 파일 시스템 등은 사용자모드에서 실행 불가능하다.

컴퓨터 시스템은 CPU 내부에 모드비트(mode bit)를 두어 프로그램을 감시하는데, 모드비트가 0이면 커널모드로, 1이면 사용자모드로 명령을 수행한다. CPU는 보안과 관련된 명령을 수행하기 전에 항상 모드비트 값을 조사한다. 예를 들어 인터럽트/시스템 콜/예외상항이 발생할 때 모드비트는 자동으로 0으로 세팅되어 운영체제는 서비스에 필요한 모든 종류의 명령을 수행할 수 있게 되고, 작업이 끝나면 모드비트를 다시 1로 만들어 사용자 프로그램에게 CPU를 넘겨준다.

</details>

<details>
<summary>sar 명령어</summary>

리눅스 시스템에서 프로세스가 사용자 모드와 커널 모드 중 어느 쪽에서 실행되고 있는지 비율을 확인하려면 sar 명령어를 사용한다. 이때 idle 상태는 CPU 코어상에 프로세스도, 커널도 움직이고 있지 않은 상태인 것을 의미한다.

</details>

<details>
<summary>프로그램 구조</summary>

컴퓨터 프로그램은 언어와 상관 없이 함수들로 구성된다. 하나의 함수가 수행되는 중에 다른 함수를 호출하고, 호출된 함수의 수행이 끝나면 다시 원래 위치로 돌아간다.

프로그램이 CPU에서 명령을 수행하려면 해당 명령은 담은 프로그램의 주소 영역이 메모리에 올라가 있어야 한다. 주소 영역은 Code, Data, Stack 영역으로 구분된다.

Code 영역은 작성한 프로그램 함수들의 코드가 CPU에서 수행할 수 있는 기계어 명령 형태로 변환되어 저장되어있는 부분이다.

Data 영역은 전역 변수 등 프로그램이 사용하는 데이터를 저장하는 부분이다.

Stack 영역은 함수가 호출될 때 호출된 함수의 수행을 마치고 복귀할 주소 및 데이터를 임시로 저장하는 데 사용되는 공간이다. 프로그램은 메인함수에서 시작해 다른 함수를 호출하면 CPU가 메인함수의 코드를 수행하다가 다른 함수의 코드로 수행위치를 옮기는데, 이때 돌아와야 하는 지점을 Stack 영역에 저장한다.
</details>

<details>
<summary>시스템의 작동 개요</summary>

CPU는 인간의 뇌처럼 스스로 생각하고 판단할 수 없다. CPU는 빠른 속도로 처리하는 계산 능력을 가지고, 매 시점 메모리의 특정 주소에 존재하는 명령을 하나씩 읽어와 그대로 실행한다.

이때 CPU가 수행해야 할 메모리 주소를 담고 있는 레지스터를 프로그램 카운터라고 부른다. CPU는 매번 프로그램 카운터가 가리키는 메모리 위치의 명령을 처리하는 것이다.

일반적으로 조건문, 반복문, 함수호출 등에 의한 주소 이동이 없는 이상 프로그램 카운터는 항상 바로 다음 명령을 가리키게 되어 코드의 순차적인 수행이 일워진다.

프로세스의 주소 공간은 위처럼 코드, 데이터, 스택 영역으로 구성되는데 각각의 프로그램마다 이러한 주소 공간을 별도로 가지고 또한 프로그램마다 독자적으로 존재하는 이러한 주소 공간을 가상 메모리 또는 논리적 메모리라고 부른다. 이는 실제 물리적 메모리의 주소와 독립적으로 각 프로그램이 독자적인 주소 공간을 가지기 때문이다.
</details>

<details>
<summary>프로세스</summary>

프로세스란 실행 중인 프로그램을 뜻한다. 프로그램이 메모리에 올라가서 실행되기 시작하면 생명력을 갖는 프로세스가 된다.

프로세스의 상태는 실행, 준비, 봉쇄의 세 가지로 구분할 수 있다. 실행 상태는 프로세스가 CPU를 보유하고 기계어 명령을 실행하고 있는 상태이고, 준비 상태는 프로세스가 CPU만 보유하면 당장 명령을 실행할 수 있지만 CPU를 할당받지 못한 상태, 봉쇄 상태는 CPU를 할당받더라도 당장 명령을 실행할 수 없는 상태이다. 이 밖에도 시작(프로세스가 시작되어 각종 자료구조를 생성했지만 메모리 획득을 승인 받지 못한) 상태나 완료(프로세스가 종료되었으나 프로세스와 관련된 자료구조를 완전히 정리하지 못한) 상태가 있다.

실행 상태에서 CPU의 제어권을 갖고 있던 프로세스가 실행되는 중 타이머 인터럽트가 발생되면 CPU의 제어권은 운영체제로 이양되고, 수행 중이던 프로세스의 문맥을 저장하고 준비 상태에 있는 프로세스 중에서 새롭게 CPU의 제여권을 부여할 프로세스를 선택하며 기존의 프로세스는 준비 상태로 변하는데, 원래 프로세스의 문맥을 저장하고 새로운 프로세스의 문맥을 세팅하는 과정을 문맥 교환(Context switch)이라고 한다.
</details>

<details>
<summary>idle 프로세스</summary>

CPU에는 '아무것도 하지 않는' 특수한 프로세스가 동작하는데, 이를 idle 프로세스라고 한다.

</details>

<details>
<summary>프로세스 제어블록(PCB)</summary>

프로세스 제어블록은 운영체제가 시스템 내의 프로세스들을 관리하기 위해 프로세스마다 유지하는 정보들을 담는 커널 내의 자료구조를 뜻한다. PCB는 아래와 같은 요소들로 구성된다.

* 프로세스의 상태 : CPU를 할당해도 되는지 결정하기 위해
* 프로그램 카운터의 값 : 다음에 수행할 명령의 위치를 찾기 위해
* CPU 레지스터의 값 : CPU 연산을 위해 현 시점에 어떤 값을 저장하고 있는지
* CPU 스케줄링 정보, 메모리 관리 정보 : CPU 스케줄링과 메모리 할당을 위해
* 자원 사용 정보 : 사용자에게 자원 사용 요금을 계산해 청구하기 위해
* 입출력 상태 정보 : 프로세스가 오픈한 파일 정보 등의 I/O 상태 정보

</details>

<details>
<summary>프로세스의 문맥교환(Context switch)</summary>

프로세스는 시분할 시스템에서 교체가 빈번하기 때문에 문맥을 가지는데, 주소 공간, 레지스터의 값, 시스템 콜 등을 통해 커널에서 수행한 일의 상태, 커널이 관리하는 각종 정보, PCB와 커널 스택 등이 문맥의 요소가 된다.

문맥교환이란 하나의 사용자 프로세스로부터 다른 사용자 프로세스로 CPU의 제어권이 이양되는 과정을 말한다. 프로세스가 바뀔 때, 기존의 프로세스의 문맥은 자신의 PCB에 저장하고, 새롭게 CPU를 할당받을 프로세스는 자신의 문맥을 PCB로부터 실제 하드웨어로 복원시킨다.

하지만 모든 인터럽트나 시스템 콜 발생 시에 문맥교환이 일어나지는 않는다. 문맥교환에는 많은 오버헤드가 따르기 때문에 모드 변경을 하는 방식으로 우회한다. 타이머 인터럽트나 I/O 시스템 콜로 인한 봉쇄 상태에서는 문맥교환이 일어난다.

</details>

<details>
<summary>프로세스의 생성</summary>

운영체제가 프로세스 전부를 생성하지는 않는다. 최초의 프로세스는 운영체제가 직접 생성하지만, 그다음부터는 이미 존재하는 프로세스가 다른 프로세스를 복제 생성한다. 이를 부모 프로세스/자식 프로세스로 구분한다. 자식 프로세스를 생성하면 부모 프로세스와는 별도의 주소 공간을 가지며, 처음에는 부모 프로세스의 주소 공간 내용을 그대로 복사해서 생성하는데, 자식 프로세스가 다른 프로그램을 수행하기 위해서는 생성된 주소 공간 위에 새로운 프로그램의 주소 공간을 덮어씌워 실행한다.

유닉스에서는 fork() 시스템 콜을 통해 새로운 프로세스를 복제 생성할 수 있는데, 이때 프로세스 ID를 제외한 모든 정보를 그대로 복사한다. fork()로 생성된 자식 프로세스는 exec() 시스템 콜을 통해 새로운 프로그램을 주소 공간을 덮어씌운다. 프로세스는 자식이 먼저 모두 종료되는데, 모든 프로세스의 종료 코드에는 exit()라는 시스템 콜이 존재한다. 명시적으로 호출하지 않아도 컴파일러가 자동으로 삽입한다.

프로세스가 fork() 시스템 콜을 하면, CPU의 제어권이 커널로 넘어가고 커널은 fork()를 호출한 프로세스를 복제(같은 문맥을 가진)해 자식 프로세스를 생성한다. 따라서 자식 프로세스는 부모 프로세스의 처음부터 수행을 다시 시작하는 게 아니라 부모 프로세스가 현재 수행한 시점(**프로그램 카운터 지점**)부터 수행한다. fork() 함수의 결과값으로 원본은 양수를 가지고 복제본에게는 0을 준다. 하지만, 자식 프로세스는 결국 부모와 모두 동일한 코드의 내용을 가질 수밖에 없으므로 이때 exec() 시스템 콜을 사용한다. exec()는 자식의 주소 공간을 완전히 새로운 프로그램으로 덮어 씌우고 첫 부분부터 다시 시작하도록 하는 시스템 콜이다. 만약 동기화가 필요한 경우는 wait() 시스템 콜을 통해 자식 프로세스가 종료될 때까지 부모 프로세스를 봉쇄 상태에 머무르게 할 수 있다.

프로세스의 생성과 관련된 fork(), exec(), exit() 등은 사용자 프로세스가 직접 수행할 수 없는 특권명령이므로 시스템 콜을 통해서만 수행 가능하다.

</details>

<details>
<summary>프로세스의 협력</summary>

프로세스는 각자 자신만의 독립적인 주소 공간을 가지고 수행되므로 원칙적으로 서로 영향을 미칠 수 없다. 하지만 협력이 필요한 경우가 있는데, 그럴 때는 운영체제가 제공하는 IPC(Inter-Process Communication) 매커니즘을 사용한다. IPC란 하나의 컴퓨터 안에서 실행 중인 서로 다른 프로세스 간에 발생하는 통신이다. IPC에서는 의사소통과 동기화를 보장해야 한다.

IPC의 대표적인 방법으로는 메세지 전달 방식과 공유메모리 방식이 있다. 메세지 전달 방식은 프로세스 간에 공유 데이터를 사용하지 않고 커널에 의해 send(message)와 receive(message)라는 두 가지 연산을 통해 수행된다. 공유메모리 방식에서는 프로세스들이 주소 공간 일부를 공유한다. 운영체제의 공유메모리를 사용하는 시스템 콜을 통해 서로 다른 프로세스들이 그들의 주소 공간 중 일부를 공유할 수 있다.

</details>

<details>
<summary>디스패처</summary>

새롭게 선택된 프로세스가 CPU를 할당받고 작업을 수행할 수 있또록 환경설정을 하는 운영체제의 코드를 디스패처라고 부른다. 디스패처는 현재 수행 중이던 프로세스의 문맥을 그 프로세스의 PCB에 저장하고 새롭게 선택된 프로세스의 문맥을 PCB로부터 복원한 후 그 프로세스에게 CPU를 넘기는 과정을 수행한다. 디스패처가 하나의 프로세스를 정지시키고 다른 프로세스에게 CPU를 전달하기까지 걸리는 시간을 디스패치 지연시간이라고 하며, 대부분은 문맥교환 오버헤드에 해당된다.

</details>

<details>
<summary>CPU 이용율</summary>

CPU 이용율은 전체 시간 중에서 CPU가 일을 한 시간의 비율을 말한다. CPU는 대부분의 시스템에 하나만 존재하는 고비용의 자원이므로 CPU 이용율은 시스템 전체의 성능과 밀접하게 관련되며, 일을 하지 않고 휴면(idle) 상태에 머무르는 시간을 최대한 줄이는 것이 스케줄링의 중요한 목표가 된다.

</details>

<details>
<summary>처리량</summary>

처리량은 주어진 시간 동안 준비 큐에서 기다리고 있는 프로세스 중 몇 개를 끝마쳤는지(CPU 버스트를 완료한 프로세스의 개수)를 나타낸다.

</details>

<details>
<summary>소요시간</summary>

소요시간은 프로세스가 CPU를 요청한 시점부터 자신이 원하는 만큼 CPU를 다 쓰고 CPU 버스트가 끝날 때까지 걸린 시간, 즉 기다린 시간과 실제로 CPU를 사용한 시간의 합을 뜻한다.

</details>

<details>
<summary>대기시간</summary>

대기시간은 CPU 버스트 기간 중 프로세스가 준비 큐에서 CPU를 얻기 위해 기다린 시간의 합을 뜻한다.

</details>

<details>
<summary>응답시간</summary>

응답시간은 프로세스가 준비 큐에 들어온 후 첫 번째 CPU를 획득하기까지 기다린 시간을 뜻한다. 이는 사용자 입장에서 가장 중요한 성능 척도이다.

</details>

<details>
<summary>스케줄링 알고리즘</summary>

* 선입선출(First-Come First-Served) 방식은 프로세스가 준비 큐에 도착한 시간 순서대로 CPU를 할당하는 방식이다. 평균 대기시간이 길어지고 대기시간과 이용률도 동반 하락한다.
* 최단작업 우선(Shortest-Job First) 방식은 CPU 버스트가 가장 짧은 프로세스에게 제일 먼저 CPU를 할당하는 방식이다. 평균 대기시간을 가장 짧게 한다. 하지만 CPU 버스트가 긴 프로세스는 준비 큐에서 무한정 기다려야하는 문제가 발생한다.
* 우선순위(Priority) 방식은 준비 큐에서 기다리는 프로세스들 중 우선순위가 가장 높은 프로세스에게 먼저 CPU를 할당하는 방식이다. 기아 현상(무한 대기)을 방지하기 위해 노화(기다리는 시간 > 우선순위 높이기) 기법을 사용할 수 있다.
* 라운드 로빈(Round Robin)은 각 프로세스가 CPU를 연속적으로 사용할 수 있는 시간을 특정 시간을 제한하는 방식이다. 할당시간이 너무 짧으면 문맥교환의 오버헤드가 커진다. CPU 버스트 시간이 균일한 경우는 FCFS가, 그렇지 않은(오히려 그렇지 않은 경우가 제너럴하다) 경우에는 라운드 로빈 방식이 효율적이다.
* 멀티레벨 큐(Multi-level Queue) 방식은 준비 큐를 여러 개로 분할해 여러 줄로 관리하는 방식이다. 빠른 응답이 필요한 대화형 작업 큐에는 라운드 로빈을, 계산 위주의 작업을 위한 큐에는 FCFS 방식을 사용한다.
* 멀티레벨 피드백 큐(Multilevel Feedback Queue) 방식은 멀티레벨 큐와 비슷하지만 프로세스가 하나의 큐에서 다른 큐로 이동 가능하다는 점에서 다르다.
* 다중처리기(Multi-processor) 방식은 CPU가 여러 개인 시스템에서 사용하는 방식이다.프로세스를 준비 큐에 한 줄로 세워서 각 CPU가 알아서 다음 프로세스를 꺼내어가도록 하거나, 각 CPU 별로 여러 줄로 세울 수 있다.
* 실시간(Realtime) 환경에서의 스케줄링은 데드라인의 개념이 존재한다. 먼저 온 요청을 처리하기보다는 데드라인이 얼마 남지 않은 요청을 먼저 처리하는 EDF(Earlist Deadline First) 방식을 사용한다.

</details>

<details>
<summary>메모리 주소</summary>

메모리는 주소를 통해 접근하는 저장장치이다. 컴퓨터는 이진수를 사용하므로 메모리 주소 또한 이진수로 매겨지게 되는데, 흔히 사용하는 컨퓨터 시스템은 32비트 혹은 64비트의 주소 체계를 사용하고 있다. 32비트의 주소 체계를 사용할 경우 2의 32승의 서로 다른 메모리 위치를 구분할 수 있다.
컴퓨터는 byte 단위로 메모리 주소를 부여하기 때문에 32비트 주소 체계를 사용하면 2의 32승 바이트만큼의 메모리 공간에 서로 다른 주소를 할당할 수 있다. 하지만 컴퓨터상의 주소는 효율적인 운영을 위해 연속된 일련의 영역을 행정구역처럼 묶어서 사용하는데, 보통 4KB(2의 12승 byte)단위로 묶어서 페이지라는 하나의 구역을 만든다.

프로그램이 실행을 위해 메모리에 적재되면 독자적인 주소 공간이 생성되는데 이를 **논리적 주소** 혹은 가상 주소라고 부른다.CPU는 프로세스마다 독립적으로 갖는 논리적 주소에 근거해 명령을 실행한다. **물리적 주소**는 물리적 메모리에 실제로 올라가는 위치를 말하는데, 보통 물리적 메모리의 낮은 주소 영역에는 운영체제가 올라가고 높은 주소 영역에 사용자 프로세스들이 올라간다.
</details>

<details>
<summary>메모리 주소 바인딩</summary>

프로세스의 논리적 주소를 물리적 메모리 주소로 연결시켜주는 작업을 주소 바인딩이라고 하고, 물리적 메모리의 주소가 결정되는 시기에 따라 세 가지로 분류한다.

* 컴파일 타임 바인딩 : 컴파일 타임에 절대주소로 적재하는 방식이며 물리적 메모리의 위치를 변경하고 싶으면 컴파일을 다시 해야 한다.
* 로드 타임 바인딩 : 프로그램의 실행이 시작될 때 물리적 메모리 주소가 결정되는 방식이며 로더(loader - 사용자 프로그램을 메모리에 적재시키는 프로그램)의 책임하에 물리적 메모리 주소가 부여되며 프로그램이 종료될 때까지 물리적 메모리상의 위치가 고정된다.
* 실행시간 바인딩 : 주소 매핑 테이블을 통해 바인딩을 점검하며 MMU(Memory Management Unit)이라는 하드웨어적인 자원이 뒷받침되어야 한다.

</details>

<details>
<summary>메모리 관리 장치(MMU)</summary>

MMU는 아주 복잡한 하드웨어인데, 프로그램은 가상 주소를 사용해 작성되고 MMU는 가상 주소를 물리 주소로 변환한다.

</details>

<details>
<summary>동적 로딩</summary>

동적로딩은 여러 프로그램이 동시에 메모리에 올라가서 수행되는 다줄 프로그래밍 환경에서 메모리 사용의 효율성을 높이기 위해 사용하는 기법 중 하나이다. 동적로딩에서는 프로세스가 시작될 때 그 프로세스의 주소 공간 전체를 메모리에 다 올려놓는 것이 아니라 메모리를 좀 더 효율적으로 사용하기 위해 해당 부분이 불릴 때 그 부분만을 메모리에 적재하는 방식을 사용한다.

동적로딩 기법은 운영체제의 특별한 지원 없이 프로그램 자체에서 구현이 가능하며 운영체제가 라이브러리를 통해 지원할 수도 있다.

</details>

<details>
<summary>동적연결</summary>

연결(linking)이란 프로그래머가 작성한 소스 코드를 컴파일하여 생성된 목적 파일(object file)과 이미 컴파일된 라이브러리 파일들을 묶어 하나의 실행파일을 생성하는 과정을 말한다.

과거에는 라이브러리를 단지 필요한 함수가 들어 있는 파일로 간주해서 프로그램의 나머지 부분과 직접 연결해 실행 파일을 만드는 **정적 연결** 방식을 사용했지만, 여러 프로그램이 똑같은 라이브러리를 사용하는 경우가 많다는 사실을 발견했다.

동적 연결은 컴파일을 통해 생성된 목적 파일과 라이브러리 파일 사이의 연결을 프로그램의 실행 시점까지 지연시키는 기법이다. 정적연결에서는 프로그래머가 작성한 코드와 라이브러리 코드가 모두 합쳐져서 실행파일이 생성된다. 또한 동적 연결은 공유 라이브러리를 사용한다. MMU가 여러 프로그램이 같은 라이브러리를 공유할 수 있게 해준다.

동적연결을 가능하게 하기 위해 실행파일의 라이브러리 호출 부분에 해당 라이브러리 위치를 찾기 위한 스텁 코드를 둔다. 라이브러리 호출 시 스텁을 통해 해당 라이브러리가 메모리에 이미 존재하는지 살펴보고 그럴 경우 그 주소의 메모리 위치에서 직접 참조하며 그렇지 않을 경우 디스크에서 동적 라이브러리 파일을 찾아 메모리로 적재한 후 수행한다. 다수의 프로그램이 공통으로 사용하는 라이브러리를 메모리에 한 번만 적재하므로 메모리 사용의 효율성을 높일 수 있고, 운영체제의 지원을 필요로 한다.

프로그램에는 진입점이 있다. 진입전은 프로그램의 첫 번째 명령어가 위치한 주소를 뜻한다. 하지만 실제로 프로그램이 실행될 때 가장 먼저 실행되는 명령어는 진입점에 있는 명령어가 아니라, 프로그램이 이루는 모든 부분이 하나로 합쳐져서 실행파일을 이룰 때 런타임 라이브러리가 추가되는데, 이 런타임 라이브러리에 있는 명령어가 먼저 실행된다.

</details>

<details>
<summary>ldd</summary>

리눅스 시스템에서 ldd 명령어로 프로그램이 어떠한 라이브러리를 링크하고 있는지 확인할 수 있다. 

최근에는 C 언어를 직접 사용하는 개발자가 드물어졌지만, OS 레벨에서는 매우 중요한 언어임을 ldd 명령어로 링크를 확인해보면 알 수 있다.

</details>

<details>
<summary>물리적 메모리 할당 방식</summary>

* 연속할당 : 물리적 메모리를 다수의 분할로 나누어 하나의 분할에 하나의 프로세스를 적재
  * 고정분할
  * 가변분할
    * 동적 메모리 할당 문제 -> First-fit, Best-fit, Worst-fit
* 불연속할당 : 하나의 프로세스를 물리적 메모리의 여러 영역에 분산해 적재
  * 페이징
  * 세그먼테이션
  * 페이지드 세그먼테이션

</details>

<details>
<summary>페이지 부재</summary>

가상메모리 기법에서는 일부 페이지만 메모리에 올라와 있고 나머지는 디스크의 스왑 영역에 존재한다. 이 시스템에서 특정 프로세스의 페이지 중 어떤 페이지가 메모리에 존재하고, 존재하지 않는지 구별하기 위해 유효-무효 비트를 두어 각 페이지에 메모리에 존재하는지 표시한다. 이때, CPU가 참조하려는 페이지가 현재 메모리에 올라와 있지 않아 유효-무효 비트가 무효로 세팅되어 있는 경우를 **페이지 부재(page fault)라고 한다.

CPU가 무효 페이지에 접근하면 주소 변환을 담당하는 MMU가 페이지 부재 트랩을 발생시키면서 CPU의 제어권이 커널모드로 전환되고, 운영체제의 페이지 부재 처리 루틴이 호출되어 부재를 처리한다.

페이지 부재가 발생하면 요청된 페이지를 디스크로부터 메모리로 읽어오는 막대한 오버헤드가 발생한다.

</details>

<details>
<summary>페이지 교체 알고리즘</summary>

* 최적 페이지 교체 : 어떠한 순서로 참조될지 미리 알고 있다는 전제하의 최적 알고리즘이므로 다른 알고리즘의 성능에 대한 상한선을 제공한다.
* 선입선출(FIFO)
* LRU(Least Recently Used) : 가장 오래전에 참조가 일어난 페이지를 쫓아낸다.
* LFU(Least Frequency Used) : 과거에 참조가 가장 적었던 페이지를 쫓아낸다.
* 클럭(Not Used Recently) : 가장 오랫동안 참조되지 않은 페이지를 교체한다. 대부분의 시스템에서 채택한다.

</details>

<details>
<summary>스레싱</summary>

프로세스가 원활하게 수행되기 위해서는 일정 수준 이상의 페이지 프레임을 할당받아야 하는데, 최소한의 페이지 프레임을 할당받지 못할 경우 성능상의 심각한 문제가 발생할 수 있다. 집중적으로 참조되는 페이지들의 집합을 메모리에 한꺼번에 적재하지 못하면 페이지 부재율이 크게 상승해 CPU 이용률이 급격히 떨어지는데, 이를 스레싱(thrashing)이라 한다.

CPU의 이용률이 낮을 경우 준비 큐가 비는 경우가 발생한다는 뜻인데, 이 경우 CPU는 메모리에 올라가는 프로세스의 수를 늘린다. 즉, MPD(Multi-Programming Degree)가 높아 지는데 MPD가 과도하게 높아지면 각 프로세스에게 할당되는 메모리의 양이 지나치게 감소한다. 그렇게 되면 각 프로세스는 그들이 원할하게 수행하기 위해 필요한 최소한의 페이지 프레임도 할당받지 못하는 상태가 되어 페이지 부재가 빈번하게 발생한다. 페이지 부재가 발생하면 디스크 I/O 작업을 수반하므로 문맥교환을 통해 다른 프로세스에게 CPU가 이양되는데, 이때 다른 프로세스 역시 할당받은 메모리 양이 지나치게 적으면 페이지 부재가 발생할 수밖에 없다. 이 과정이 반복되고
준비 큐에 있는 모든 프로세스가 다 페이지 부재를 발생시키면, CPU 이용률이 급격하게 떨어진다. 이 과정이 반복되는 상황을 스레싱이라고 한다.

</details>

<details>
<summary>워킹셋 알고리즘</summary>

프로세스는 일정 시간 동안 특정 주소 영역을 집중적으로 참조하는 경향이 있는데, 이렇게 집중적으로 참조되는 페이즈들의 집합을 지역성 집합이라고 한다. 워킹셋 알고리즘은 이러한 지역성 집합이 메모리에 동시에 올라갈 수 있도록 보장하는 메모리 관리 알고리즘을 뜻한다.

워킹셋 알고리즘에서는 프로세스가 일정 시간 동안 원활히 수행되기 위해 한꺼번에 메모리에 올라와 있어야 하는 페이지들의 집합을 워킹 셋이라고 정의하고, 프로세스의 워킹셋을 구성하는 페이지들이 한꺼번에 메모리에 올라갈 수 있는 경우에만 그 프로세스에게 메모리를 할당한다. 구체적으로는 메모리에 올라와 있는 프로세스들의 워킹셋 크기의 합이 프레임의 수보다 클 경우 일부 프로세스를 스왑 아웃시켜서 남은 프로세스의
워킹셋이 메모리에 모두 올라가는 것을 보장하여 MPD를 줄인다. 반면 프로세스들의 워킹셋을 모두 할당한 후에도 프레임이 남을 경우 스왑 아웃되었던 프로세스를 다시 메모리에 올려서 워킹셋을 할당함으로써 MPD를 증가시킨다. 이러한 방식으로 워킹셋 알고리즘은 CPU 이용률을 높게 유지하면서 MPD를 적절히 조절해 스레싱을 방지한다.

</details>

<details>
<summary>디스크의 구조</summary>

디스크 외부에서는 디스크를 일정한 크기의 저장공간들로 이루어진 1차원 배열로 취급하게 되는데, 이 일정한 크기의 공간을 논리블록이라고 하며 디스크에 데이터가 저장될 때는 논리블록 단위로 저장되고 내부 및 외부 입출력 시에도 동일하다.

논리블록에 저장된 데이터를 접근하기 위해서는 배열에 접근하는 것처럼 해당 블록의 인덱스 번호를 디스크에 전잘해야 한다. 디스크 컨트롤러는 해당 논리블록이 저장된 물리적 위치를 찾아 요청된 데이터에 대한 입출력 작업을 수행하게 되고, 논리블록이 저장되는 디스크 내의 물리적인 위치를 **섹터**라고 부른다.

디스크의 물리적인 구조는 마그네틱의 원판으로 구성된다. 하나의 디스크 내에 원판의 수는 1개 이상이다. 각 원판은 트랙으로 구성되고, 트랙은 섹터로 나뉜다. 여러 개의 원판에서 상대적 위치가 동일한 트랙들의 집합을 실린더라 부른다.

</details>

<details>
<summary>아이노드</summary>

아이노드는 디스크 블록에 대한 인덱스(Index)와 노드(Node)를 합친 단어다. 아이노드에는 파일에 대한 여러 가지 정보가 들어간다. 파일 이름, 파일 소유자, 파일 크기, 파일에 대한 허가 내역 등이 포함 된다.

</details>

<details>
<summary>디스크 스케줄링</summary>

디스크 스케줄링의 가장 중요한 목표는 디스크 헤드의 이동거리를 줄이는 것이다. 

* FCFS(First-Come, First-Served)
* SSTF(Shortest Seek Time First) : 현재의 헤드 위치로부터 가까운 곳에서 지속적인 요청이 들어올 경우 헤드 위치에서 멀리 떨어진 곳의 요청은 무한히 기다려야 함
* SCAN : 헤드가 디스크 원판의 안쪽 끝과 바깥쪽 끝을 오가며 그 경로에 존재하는 모든 요청을 처리하는 방식 : 가운데 위치가 기다리는 시간이 짧다.
* C-SCAN : SCAN과 달리 헤드가 한쪽 끝에 도달하고 방향을 바꾼 후에는 출발점으로 다시 이동만 해서 SCAN보다 이동 거리는 길지만 좀 더 균일한 탐색시간을 제공한다.
* LOOK : 헤드가 한쪽 방향으로 이동하다가 그 방향에 더 이상 대기 중인 요청이 없으면 즉시 반대로 바꾸는 스케줄링 방식

</details>

<details>
<summary>웹캐싱 개요</summary>

캐싱 기법은 저장장치 계층 간의 속도 차이를 완충시키기 위해 다방면의 분야에서 널리 연구되었다. 1990년대 중반부터는 웹의 보편화와 CDN 서비스의 활성화로, 원격지의 객체를 캐싱하는 기법의 중요성이 커지고 있다. 특히 웹의 인기가 높아감에 따라 네트워크의 병목현상과 그로 인한 웹서비스의 지연시간 문제 등이 점점 심각해져 웹캐싱 기법에 대한 연구가 활발하다.

웹캐싱이란 웹 사용자에 의해 빈번히 요청되는 데이터를 사용자와 지리적으로 가까운 웹캐시 서버에 보관해 빠른 서비스를 가능하게 하는 기법을 말한다. 이때 웹캐싱만을 전담하는 프락시서버는 통상적으로 일개 그룹의 웹 사용자에 대한 서비스 지연시간을 줄이기 위해 사용되며, 네트워크의 대역폭 절약과 함께 웹서버의 부하를 줄이는 역할도 담당한다.

웹서버 쪽에는 역방향 프락시 캐시가 사용되는데, 이는 일개 그룹에 속한 웹서버의 객체들을 캐싱하여 서버의 부하를 직접적으로 줄이는 역할을 한다.

캐시에 보관된 웹 객체는 근원지 서버에서 변경될 수 있으므로 캐싱 시스템은 통상적으로 일관성 유지 기법을 필요로 한다. 일관성 유지 기법은 사용자가 요청한 웹 객체가 캐싱되어 있는 경우 이 객체가 근원지 서버에 있는 개체와 동일한지를 확인해서 사용자에게 최신의 정보를 전달하기 위해 필요하다.

웹캐시의 교체 알고리즘은 근원지 서버의 위치 및 특성에 따라 객체를 캐시로 읽어오는 비용이 다르고, 하나의 URL에 대응하는 파일 단위로 캐싱이 이루어지기 때문에 캐싱 단위 크기가 균일하지 않는 이질성을 고려해야 한다.

</details>

<details>
<summary>부트스트랩(bootstrap)</summary>

컴퓨터를 부팅하는 과정은 롬 등에 들어 있는 작은 프로그램을 메모리로 읽어오는 것부터 시작한다. 이 프로그램은 필요한 초기화를 진행한 후 더 큰 프로그램을 읽어오고, 이 프로그램은 더 큰 운영체제 등을 불러올 수 있다. 초기 컴퓨터에서는 사람이 직접 전면 패널 스위치를 사용해 최초 부트스트랩 프로그램을 입력했다.

</details>

<details>
<summary>웹브라우저</summary>

웹 브라우저는 그 자체가 가상 머신이다. 웹 브라우저는 아주 복잡한 명령어 집합을 완전히 소프트웨어로만 구현한 추상적인 컴퓨터다. 즉, 인터프리터에 속한다.

</details>

<details>
<summary>교착상태(Dead Lock)</summary>

두 개 이상의 작업이 공유 자원을 두고 상대방의 작업이 끝나기만을 기다리는 상태. 교착 상태는 아래의 네 가지 조건을 동시에 만족하면 발생한다.

* 상호 배제 : 공유자원을 함께 쓸 수 없어서 한 프로세스가 독점적으로 사용해야 한다
* 점유 대기 : 프로세스들은 어느 자원을 점유한 상태에서 다른 자원을 요청한다
* 비선점 : 프로세스가 할당받은 자원을 강제로 빼앗을 수 없다
* 순환 대기 : 각 프로세스가 서로 순환적으로 다른 프로세스가 갖고 있는 자원을 요구한다

</details>

출처. 
* 운영체제와 정보기술의 원리, 반효경
* 한 권으로 읽는 컴퓨터 구조와 프로그래밍, 조너선 스타인하트
* 실습과 그림으로 배우는 리눅스 구조, 다케우치 사토루