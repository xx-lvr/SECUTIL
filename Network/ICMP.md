## ICMP란?
**ICMP(Internet Control Message Protocol)** 는
IP 네트워크에서 발생하는 **오류 상황 및 제어 정보를 전달하기 위한 프로토콜**이다.\
주로 **오류 메시지와 네트워크 상태 정보**를 전달하는 데 사용된다.

## ICMP 용도
ICMP의 가장 큰 용도는 **오류 보고 및 네트워크 진단**이다.\
라우터나 호스트가 IP 패킷 처리 중 문제가 발생했을 때,\
그 사실을 송신자에게 알리기 위해 사용된다.

## ICMP 기능
- IP 프로토콜을 이용하여 ICMP 메시지 전달
- 네트워크 계층(Layer 3)에 속함
- 네트워크 상태 및 오류 정보 전달 역할 수행
- **종단 간 데이터 전송 역할은 수행하지 않음**

## ICMP 작동 방식
- IP 패킷 처리 중 오류 발생
- 오류를 감지한 장비(라우터/호스트)가 ICMP 메시지 생성
- ICMP 메시지를 IP 패킷에 실어 송신자에게 전달

## ICMP 활용 예
- `ping` : ICMP Echo Request / Echo Reply
- `traceroute` : ICMP Time Exceeded 메시지 활용