# H_SOK_yang

# 컴퓨터는 어떻게 동작할까?

## [탐구활동 1] 컴퓨터는 무엇일까요? 여러분 스스로 컴퓨터에 대해 정의를 내려 봅시다.

1. 영상 "다양한 반복적인 작업을 대신 해줌"
2. 마늘 "생각을 현실화해주는 도구"
3. 눙이 "인간의 한계를 보완해주는 물건"
4. 다다 "귀찮은 일을 빨리 해주는 기계"
5. 양갱 "다양함(즐거움, 복잡함 등)을 주는 도구 / 여가를 즐길 수 있는, 버거운 일을 도와주는 용도가 되기도"

## [탐구활동 2] 여러분이 생각하는 컴퓨터와 동일하게 동작하는 디바이스들을 일상에서 찾아 봅시다. 

1. 닌텐도: 옆으로 이동하는 버튼을 누르면 기기 내부에서 입력값에 대한 계산을 완료한 뒤, 화면에 행동이 출력된다.
2. 스마트폰: 내가 원하는 결과를 화면을 터치해서 입력하고 그 정보를 처리해 화면으로 띄워줌. 
3. 노래방 기계: 자판은 키보드와 같은 역할을 하고, 그 정보를 중앙 장치에서 처리를 해서 모니터로 내가 선택한 노래를 출력한다. 

## [탐구활동 3] What is the difference between register and transistor?

Answer : Register is one kind of concept of memory that can store data or command temporarily while CPU executes operation processing. Register is composed of a bunch of Flip-Flops which is a circuit that can store and maintain information of 1 bit. A value of 1 bit is decided by whether current flows to transistor.

답변 번역 : 레지스터는 CPU가 연산 처리를 실행시에 데이터나 명령을 “일시적"으로 기억할 수 있는 메모리 개념. 레지스터는 플립플롭으로 구성되어 있음. 플립플롭은 1 비트의 정보를 보관, 유지할 수 있는 회로이고 1 비트는 트렌지스터에 전류가 흐르는지 흐르지 않는지에 따라 비트의 값(0 또는 1)이 결정됨 

### 문제와 관련된 지식
* 트랜지스터 : 스위치 작용(전류가 흐르거나 흐리지 않게 함)을 통해 전압의 유무로 인하여 비트의 값을 결정

* 플립플롭(Flip-Flop) : 1 비트의 정보를 보관, 유지할 수 있는 회로이다. 신호가 들어오지 않는 한 이전값을 보유하는 성질을 지님. (플립플롭을 통해 CPU가 32비트인지 64비트인지 결정이 되는건가? -> 공부 필요)

* 레지스터 : 소량의 데이터 혹은 처리중인 작업의 중간 결과를 일시적으로 기억해두는 저장장치. 플립플롭으로 구성 됨

* 레지스터 : 메모리 계층의 최상위에 위치하며, 가장 빠른 속도로 접근 가능한 메모리이다. 컴퓨터의 주기억 장치는 데이터와 명령을 기억하고 있을 뿐이다. 그래서 산술 연산, 논리 연산, 전송 조작을 행할 때 데이터나 명령을 일시적으로 기억해둘 장소가 필요하게 되고, 용도에 따라서 여러 가지 레지스터가 있다. 주요한 레지스터에는 누산기(accumulator), 연산 레지스터(arithmetic register), 명령 레지스터(instruction register), 자리 이동 레지스터(shift register), 지표 레지스터(index register) 등이 있고, 또한 이들 레지스터는 보통 중앙 처리 장치 안에 있다.

* 레지스터 - CPU 옆에 붙어 있음. (팩맨께서는 Ram에 있다고 하셨지만 내가 조사하기로는 CPU에 있다고 나와 있음.)
1. CPU가 요청을 처리하는데 필요한 데이터를 일시적으로 저장하는 기억장치이다.
2. CPU에서 처리한 연산의 결과를 Ram으로 보내고 영구적으로 데이터를 저장해야 하는 등의 명령을 처리하기 위해서 이들에 대한 주소와 명령의 종류를 저장할 수 있는 기억공간
3. 2번과 같은 작업을 처리하기 위해 메모리(Ram)보다 빨라야함. (=레지스터는 공간은 작지만 CPU와 직접 연결되어 있으므로 연산속도가 메모리보다 실제 수십 배에서 수백배까지 빠르다.) 
4. 그리고 CPU는 자체적으로 데이터를 저장할 방법이 없기 때문에 메모리로 직접 데이터를 전송할 수 없다. 따라서 연산을 읽기 위해서는 반드시 레지스터를 거쳐야하며, 이를 위해서는 레지스터는 특정 주소를 가리키거나 값을 읽어올 수 있다.

### 부가적으로 컴퓨터를 이해하는데 도움되는 지식

* CPU : 다양한 연산 수행. 만약 CPU가 곱셈 연산시 중간 과정값을 저장해야할때 잠시 저장해야하는 메모리가 필요한데 이것이 플립플롭이다. 이를 통해 중간 값을 저장해 둘 수 있게 되었다. CPU에서 이렇게 빠르게 연산도중에 값을 저장해두고 사용하는 메모리를 레지스터라고 한다.
 * 메모리 계층 구조(Memory hierarchy)란 메모리를 필요에 따라 여러가지 종류로 나누어 둠을 의미한다[1]. 이때 필요란 대부분의 경우 CPU가 메모리에 더 빨리 접근하기 위함이다. 일반적으로 오른쪽 그림과 같이 나타낸다. 레지스터와 캐시는 CPU 내부에 존재한다. 당연히 CPU는 아주 빠르게 접근할 수 있다. 메모리는 CPU 외부에 존재한다. 레지스터와 캐시보다 더 느리게 접근 할 수 밖에 없다. 하드 디스크는 CPU가 직접 접근할 방법조차 없다. CPU가 하드 디스크에 접근하기 위해서는 하드 디스크의 데이터를 메모리로 이동시키고, 메모리에서 접근해야 한다. 아주 느린 접근 밖에 불가능하다.

* 메모리 : 흔히 Ram과 Rom을 말함. 여기서 더 자세히 나누면 Ram은 휘발성 메모리이고, Rom은 비휘발성 메모리 이다.

* Ram(=Random Access Memory) : 주기억장치, 휘발성 메모리. / 역할 : 일반적인 컴퓨터 작업의 과정을 살펴보면, 램은 하드디스크로부터 일정량의 데이터를 복사해 임시 저장한 후, 이를 필요 시마다 CPU에 빠르게 전달하는 역할을 한다. 이후부터는 속도가 느린 하드디스크는 배제하고 빠른 CPU와 램끼리만 데이터를 교환하므로 전반적인 작업을 고속으로 처리할 수 있다.  RAM은 기억된 정보를 읽어내기도 하고 다른 정보를 기억시킬 수 있는 메모리이다. 즉, 기록과 해독이 모두 가능하다. / 종류 : DRAM과 SRAM이 있음.

* Rom(=Read Only Memory) : 읽기 전용 기억장치, 비휘발성 메모리 / 역할 : Rom은 전원이 들어오면 무슨 작업을 해야할지 미리 프로그램 되어 있는 장치(=전자소자)이다. 대표적 예시로는 부팅시에 키보드/마우스 등 입력 장치를 인식하고 사용가능하 상태로 만드는 것. 이후 OS가 실행되기 위해 필요한 각종 장치 등을 메모리에 로드함.


* 마늘이 생각하는 컴퓨터의 처리 과정 (이 5단계가 가장 기본 개념이지 않을까? 라고 생각.)
1. 입력장치를 통해 뭔가 입력 —> 2. 입력된 내용이 CPU로 전달 —> 3. CPU 내부에서 연산을 처리 —> 4. Ram에 저장 or 보조기억장치(=HDD, SSD)에서 정보를 가지고 올 수도 있음.. —> 5. Ram에서 HDD or SSD로 저장 및 출력 장치로 출력.



## [탐구활동 4] HDD와 SSD의 장단점을 각각 무엇일까요? 언제 우리는 HDD를 사용해야 할까요?

1. HDD : 플래터가 회전하며 판독 및 기록을 하여 데이터를 읽고/쓰며 저장하는 비휘발성 저장 장치. 즉 데이터가 저장되면, 컴퓨터가 정료되어도 사용자가 지우거나 포맷하지 않는 이상 데이터는 항상 저장이 된 상태로 보관이 됨.
* 장점: 용량당 가격이 저렴, 대용량, 장기간 보존 가능
* 단점: 액세스 속도가 SSD보다 떨어짐, 진동/충격에 약함, 구동 부분에 있어서 소비 전력이 높고 소음과 발열을 동반
2. SSD : 하드드라이브와 수행하는 기능은 동일, 플래시 메모리 칩에 데이터가 저장이 됨. 일반적인 USB 플래시 칩과는 다른 유형이며, 하드디스크보다 더욱 빠르며 신뢰할 수 있는 구조.
* 장점: 빠른 액세스, 진동/충격에 강함, 저소음/저전력
* 단점: 용량당 가격이 높음, 용량이 작음, 읽고 쓰는 횟수에 제한이 있음, 장기간 사용하지 않으면 데이터 손실

3. 둘의 큰 차이점 : SSD의 저장 매체가 반도체 메모리라는 것.

* USB 메모리는 USB 단자에 연결하여 사용하지만, SSD는 보드에 연결하는 내장형 부품과 기판, USB 장치 등 다양한 형태로 공급되고 있다.

# Git

## [탐구활동 1] Git을 왜 사용해야 할까요? 실제 생활에서 Git과 유사한 경험을 한 적이 있다면 공유해주세요.
1. 양갱, 다다, 눙이 - 변경된 파일로 되돌아갈 수 있고, 한 폴더에서 실험적인 작업을 할 수 있는 게 간편해서 사용하는 게 아닐까 생각을 함.
2. 마늘 - 한땀 앱 개발하면서 사용하고 있는데 작업을 하다가 코드가 날라가거나 실수가 생기는데 전 버전으로 돌아갈 때 유용하더라. 

## [탐구활동 2] Git과 Github의 차이는 무엇일까요? 
1. Git
* 변경 사항 추적 시스템
2. GitHub
* 변경 사항을 추적할 수 있는 Cloud Service. 



# 인터넷은 어떻게 동작할까?

## 완성된 StudentNet을 기반으로 다음의 질문들에 대답하세요.
### 다른 사람에게 정보를 전달하기 위한 최소의 숫자는 무엇인가요? 한 친구에게 메시지를 보낼 수 있는 방법은 얼마나 있나요?
### 다른 사람과 좀 더 많이 연결 된 사람이 누구인가요?
### 다른 사람에게 정보를 전달 할 수 없는 사람도 있나요?
### 만약 한명의 친구가 아프다면 다른 친구에게 정보를 전달할 수 있는 방법이 여전히 있나요? 전달하기 위한 시간은 늘어나나요? 줄어드나요?
1. 콜라 -> 양갱 -> 다다 - 눙이 (3)  / 경우의 수가 많다.
2. 호비 (5개)
3. 모두가 전달을 할 수 있다.
4. 2명 이상의 친구와 연결이 되어야 정보를 전달 받을 수 있다. 하지만 시간이 늘어날 수 있다. 
