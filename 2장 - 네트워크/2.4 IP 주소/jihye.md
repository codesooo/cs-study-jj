# 4.1 ARP
- 컴퓨터 간의 통신은 IP 주소에서 ARP를 통해 MAC 주소를 찾아 MAC 주소를 기반으로 통신
  - ARP(Address Resolution Protocol) : IP 주소로부터 MAC 주소를 구하는 IP와 MAC 주소의 다리역할을 하는 프로토콜
  - ARP와 RARP
    
    ![image](https://github.com/codesooo/cs-study-jj/assets/129932517/b62a6853-66bb-4d23-907e-d7df0ab8f3f2)

![image](https://github.com/codesooo/cs-study-jj/assets/129932517/91aa663d-c9e2-41d8-9325-08e1e2f17c24)

    - 브로드 캐스트 : 송신 호스트가 전송한 데이터가 네트워크에 연결된 모든 호스트에 전송되는 방식
    - 유니 캐스트 : 고유 주소로 식별된 하나의 네트워크 목적지에 1:1로 데이터를 전송하는 방식


# 4.2 홉바이홉 통신
: IP 주소를 통해 통신하는 과정
- hop(홉) : 통신망에서 각 패킷이 여러 개의 라우터를 건너가는 모습을 비유적으로 표현
- 통신 장치에 있는 '라우팅 테이블'의 IP를 통해 시작 주소부터 다음 IP로 계속해서 이동하는 '라우팅' 과정을 거쳐 패킷이 최종 목적지까지 도달하는 통신

  ![image](https://github.com/codesooo/cs-study-jj/assets/129932517/46bdbad7-a472-477e-aef4-9fbbf84da38a)

## 라우팅 테이블
: 송신지에서 수신지까지 도달하기 위해 사용

라우터에 들어가 있는 목적지 정보들과 그 목적지로 가기 위한 방법이 들어 있는 리스트

## 게이트웨이
: 서로 다른 통신망, 프로토콜을 사용하는 네트워크간의 통신을 가능하게 하는 관문 역할을 하는 컴퓨터나 소프트웨어를두루 일컫는 용어

# 4.3 IP 주소 체계
|IPv4 | IPv6 |
|---|---|
|32비트를 8비트 단위로 | 64비트를 16비트 단위로|
|현재 가장 많이 쓰임 | 추세는 일로 가고 있음|

## 클래스 기반 할당 방식
![image](https://github.com/codesooo/cs-study-jj/assets/129932517/f622a9ac-8ffb-4ef4-a443-cc786645ec38)

![image](https://github.com/codesooo/cs-study-jj/assets/129932517/deb9fa76-13ca-404b-a7f5-25e35fdbaccd)

맨 앞에 있는 비트를 '구분 비트'

ex> 클래스 A : 0 , 클래스 B : 10, 클래스 C: 110

- 네트워크의 첫 번째 주소는 네트워크 주소로 사용되고 가장 마지막 주소는 브로드 캐스트용 주소로 네트워크에 속해 있는 모든 컴퓨터에 데이터를 보낼 때 사용


## DHCP
Dynamic Host Configuration Protocol
- IP 주소 및 기타 통신 매개변수를 자동으로 할당하기 위한 네트워크 관리 프로토콜
- 자동으로 IP주소 할당

## NAT
Network Address Translation
- 패킷이 라우팅 장치를 통해 전송되는 동안 패킷의 IP 주소 정보를 수정하여 IP 주소를 다른 주소로 매핑하는 방법
- 공인 IP와 사설 IP로 나눠서 많은 주소를 처리
  - IPv4 주소 체계만으로는 많은 주소들을 모두 감당하지 못한다는 단점 해결!
- NAT를 가능하게 하는 소프트웨어는 ICS, RRAS, Netfilter

  ![image](https://github.com/codesooo/cs-study-jj/assets/129932517/02f19675-11f8-4324-8feb-6e8e8b430136)

- NAT를 쓰는 이유는 주로 여러 대의 호스트가 하나의 공인 IP 주소를 사용하여 인터넷에 접속하기 위함.
- NAT를 이용한 보안 : 내부 네트워크에서 사용하는 IP주소와 외부에 드러나는 IP 주소를 다르게 유지할 수 있기 때문에 내부 네트워크에 대한 어느 정도의 보안이 가능해진다.
- NAT의 단점 : NAT는 여러 명이 동시에 인터넷을 접속하게 되므로 실제로 접속하는 호스트 숫자에 따라서 접속 속도가 느려질 수 있다.

 # 4.4 IP 주소를 이용한 위치 정보
 - IP 주소는 인터넷에서 사용하는 네트워크 주소이기 때문에 이를 통해 동 또는 구까지 위치 추적이 가능
