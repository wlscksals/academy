# ICMP

### ICMP란?

    TCP/IP에서 IP 패킷을 처리할 때 발생되는 문제를 알리거나, 진단 등과 같이
    IP 계층에서 필요한 기타 기능들을 수행하기위해 사용되는 프로토콜

> OSI 계층 위치

![333766269-42c2c89c-4bb4-441d-bdb9-9ac2ed5dfde3](https://github.com/user-attachments/assets/2bfc70c6-3442-4166-a63d-e2e94a85810a)

<br>

> 메세지 종류
    Echo request (8) : 해당 수신자가 이 메시지를 받으면 응답을 해 달라는 요청
    Echo reply (0): Echo request 를 받은 수신자가 보내주는 응답.
    Destination Unreachable (3) : 네트워크가 끊겨 있거나, 장비가 꺼져 있거나, 
    경로가 없거나 등 여러 이유로 최종 목적지에 도달할 수 없을때 보내지는 메시지
    Time Exceeded (11) : TTL 값이 감소하여 0 이 되었을때 이 메시지를 송신자에게 돌려줌
