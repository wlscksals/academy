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


<br>

> ICMP를 사용하는 명령어(프로그램)

        [Ping]
          해당 IP를 가진 장비에 접속 가능한지 확인하는 프로그램
          echo request를 던지고 echo reply를 확인
          정상적으로 echo reply를 수신할 경우
          걸린 시간을 계산하여 해당 장비까지 회선 속도를 가늠
          reply를 수신 못하거나 destination unreachable을 수신하게 되면
          해당 장비에 도달 할 수 없음을 알 수 있다.

         [Traceroute]
           해당 장비까지 가는 경로를 추척하는 프로그램
           모든 라우터는 패킷을 수신하면 TTL 을 1을 감소시키고 전달해야 하는데,
           만약 TTL 이 0 이 되면 패킷을 버리고, 대신 time exceeded 메시지를 송신측에게 돌려 주게 된다.
           이런 특성을 이용해서 처음에는 TTL = 1 로 설정하고 패킷을 쏘면,
           제일 처음 만나는 라우터가 time exceeded 메시지를 보내기에 이 라우터의 IP 주소를 알 수 있게 된다.
           그 다음 TTL = 2 로 패킷을 쏘고, 그 다음에는 TTL = 3, 4, 5, 6 ... 으로
           최종 목적지에 도달할 때까지 TTL 을 증가시키며 패킷을 쏜다.
           이를 이용하면 최종 목적지까지 가는 경로를 모두 확인 할 수 있다
