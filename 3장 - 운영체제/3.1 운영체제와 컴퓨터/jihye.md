- 운영체제 : 하드웨어와 소프트웨어(유저 프로그램)를 관리하는 일꾼
- 컴퓨터 : CPU, 메모리 등으로 이루어진

# 1.1 운영체제의 역할과 구조
## 운영체제의 역할
1. CPU 스케줄링과 프로세스 관리
  - CPU 소유권을 어떤 프로세스에 할당할지, 프로세스의 생성과 삭제, 자원 할당 및 반환을 관리

2. 메모리 관리
   - 한정된 메모리를 어떤 프로세스에 얼만큼 할당해야 하는지 관리

3. 디스크 파일 관리
   - 디스크 파일을 어떠한 방법으로 보관할지 관리

4. I/O 디바이스 관리
   - I/O 디바이스들인 마우스, 키보드와 컴퓨터 간에 데이터를 주고받는 것을 관리
  


## 운영체제의 구조
![image](https://github.com/codesooo/cs-study-jj/assets/129932517/ce88854f-22cc-4af3-9041-a28574f241c4)

- GUI
  - 사용자가 전자장치와 상호 작용할 수 있도록 하는 사용자 인터페이스의 한 형태, 단순 명령어 창이 아닌 아이콘을 마우스로 클릭하는 단순한 동작으로 컴퓨터와 상호 작용할 수 있도록 해준다.
    
- 드라이버
  - 하드웨어를 제어하기 위한 소프트웨어
 
    
- CUI
  - 그래픽이 아닌 명령어로 처리하는 인터페이스
 

### 시스템콜
운영체제가 커널에 접근하기 위한 인터페이스

유저 프로그램이 운영체제의 서비스를 받기 위해 커널 함수를 호출할 때 쓴다.

- ![image](https://github.com/codesooo/cs-study-jj/assets/129932517/6d1390cb-3239-44e4-b4c0-662c0abea67a)

- 유저모드에서 파일을 읽지 않고 커널 모드로 들어가 파일을 읽고 다시 유저 모드로 돌아가 그 뒤에 있는 유저 프로그램으 로직을 수행

  - I/O 요청 : 입출력 함수, 데이터 베이스, 네트워크, 파일접근 등에 관한 일
  - 드라이버 : 하드웨어를 제어하기 위한 소프트웨어

![image](https://github.com/codesooo/cs-study-jj/assets/129932517/ad5f1318-e735-42c1-9190-ab0672374a76)

 
- 이 시스템콜을 하나의 추상화 계층.
- 이를 통해 네트워크 통신이나 데이터베이스와 같은 낮은 단계의 영역 처리에 대한 부분을 많이 신경 쓰지 않고 프로그램을 구현할 수 있는 장점

- modebit
  - 시스템콜이 작동될 때 modebit을 참고해서 유저 모드와 커널 모드를 구분
  - modebit은 1 또는 0의 값을 가지는 플래그 변수
  - 커널 모드를 거쳐 운영체제를 통해 작동한다고 해도 100% 막을 수는 없지만, 운영체제를 통해 작동하게 해야 막기 쉽다 -> 이를 위한 장치가 modebit
  - 0은 커널 모드 1은 유저 모드
  - ![image](https://github.com/codesooo/cs-study-jj/assets/129932517/08f19141-4d4e-427e-a660-598c73647aea)

    - 그림처럼 유저 프로그램이 카메라를 이용하려고 할 때 시스템콜을 호출하고 modebit을 1에서 0으로 바꾸며 커널 모드로 변경한 후 카메라 자원을 이용한 로직을 수행
    - 이후에 modebit을 0에서 1로 바꿔서 유저 모드로 변경하고 이후 로직을 수행
      - 유저모드 : 유저가 접근할 수 있는 영역을 제한적으로 두며 컴퓨터 자원에 함부로 침범하지 못하는 몯,
      - 커널 모드 : 모든 컴퓨터 자원에 접근할 수 있는 모드
      - 커널 : 운영체제의 핵심 부분이자 시스템콜 인터페이스를 제공하며 보아, 메모리, 프로세스, 파일 시스템, I/O 디바이스, I/O 요청 관리 등 운영체제의 중추적인 역할

# 1.2 컴퓨터의 요소
컴퓨터는 CPU, DMA 컨트롤러, 메모리, 타이머, 디바이스 컨트롤러 등으로 이루어져 있다.

## CPU
산술논리연산장치, 제어장치, 레지스터로 구성되어 있는 컴퓨터 장치

- AKA. 인터럽트에 의해 단순히 메모리에 존재하는 명령어를 해석해서 실행하는 일꾼

- 제어장치
  - 프로세스 조작을 지시하는 CPU의 한 부품
  - 입츨력장치 간 통신을 제어하고 명령어들을 읽고 해석하며 데이터 처리를 위한 순서를 결정3333333333333333
 
 
- 레지스터
  - CPU 안에 있는 매우 빠른 임시기억장치
  - CPU와 연결되어 있으므로 연산 속도가 메모리보다 수십 배에서 수백 배까지 빠르다.
  - CPU는 자체적으로 데이터를 저장할 방법이 없기 때문에 레지스터를 거쳐 데이터를 전달

- 산술논리연산장치
  - 덧셈,뺄셈 같은 두 숫자의 산술 연산과 배타적 논리합, 논리곱 같은 논리 연산을 계산하는 디지털 회로

### CPU 연산 처리
![image](https://github.com/codesooo/cs-study-jj/assets/129932517/7b37c10e-ba77-422e-bed6-d0884e0863fc)

### 인터럽트
어떤 신호가 들어왓을 때 CPU를 잠깐 정지시키는 것

- 인터럽트 간에는 우선순위가 있다.

   - 인터럽트 핸들러 함수: 인터럽트가 발생했을 때 이를 핸들링하기 위한 함수. 커널 내부의 IRQ를 통해 호출되며 request_irq()를 통해 인터럽트 핸들러 함수를 등록할 수 있다.

#### 하드웨터 인터럽트
키보들르 연결한다거나 마우스를 연결하는 일 등의 IO 디바이스에서 발생하는 인터럽트

- 인터럽트 라인이 설계된 이후 순차적인 인터럽트 실행을 중지하고 운영체제에 시스템콜을 요청해서 원하는 디바이스로 향해 디바이스에 있는 작은 로컬 버퍼에 접근하여 일을 수행

#### 소프트웨어 인터럽트
= 트랩(trap)이라고도 함.

프로세스 오류 등으로 프로세스가 시스템콜을 호출할 때 발동

## DMA 컨트롤러
I/O 디바이스가 메모리에 직접 접근할 수 있도록 하는 하드웨어 장치
CPU에만 너무 많은 인터럽트 요청이 들어오기 때문에 CPU 부하를 막아 주며 CPU의 일을 부담하는 보조 일꾼

- 또한, 하나의 작업을 CPU와 DMA 컨트롤러가 동시에 하는 것을 방지
## 메모리
전자회로에서 데이터나 상태, 명령어 등을 기록하는 장치, 보통 RAM을 일컬어 메모리라고도 한다.
- CPU는 계산, 메모리는 기억
- CPU는 일꾼, 메모리는 작업장

## 타이머
몇 초 안에는 작업이 끝나야 한다는 것을 정하고 특정 프로그램에 시간 제한을 다는 역할

-> 시간이 많이 걸리는 프로그램이 작동할 때 제한을 걸기 위해 존재

## 디바이스 컨트롤러
: 컴퓨터와 연결되어 있는 IO 디바이스들의 작은 CPU를 말하고 옆에 붙어 있는 로컬 버퍼는 각 디바이스에서 데이터를 임시로 저장하기 위한 작은 메모리를 뜻 함

