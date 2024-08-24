# 라우터

### 라우터 기본
> 라우터 이미지

|전면부|![015cdc4b-58b7-4d4d-8b92-a5448f5ae320](https://github.com/user-attachments/assets/e8da0a3f-702d-45c6-9647-15adc0ab4ac9)|
|-|-|
|후면부|![a4eb6968-da69-429d-aae5-0efddf800129](https://github.com/user-attachments/assets/5e03b977-a69c-42bd-a951-01aecd44ec88)|

<br>

> 라우터 내부 구조

![1a0b833e-1fe7-476a-9e67-7c4e7bf4f9d7](https://github.com/user-attachments/assets/347c0de2-c4a4-45e8-b8e7-b863c20a2202)

<br>

> 라우터 부팅 순서

          POST(Power On Self Test)
                     ↓
             BootStrap(ROM -> RAM)
                     ↓
       IOS Loading(Flash or Network ->RAM)
                     ↓
    설정내용 Loading(NVRAM orNetwork or Console ->RAM)

<hr>
<hr>

## IOS 모드

> IOS 기본
    시스코社의 거의 모든 라우터,스위치 등 장비에서 구현된 그 회사 전용의 운영체제
    소형에서 대형장비에 이르기까지 동일한 명령어 세트, 사용자 인터페이스, 
    운영방식으로 통일성을 기함
    따라서, 하나의 장비에서 익힌 명령어를 다른 유형의 장비에서도 그대로 적용이 가능

<br>

> IOS 모드

    [사용자모드]- > 명령어의 제한적 사용 모드
    [특권모드(Privileged Mode)]-> 관리자 모드
    [설정 모드]
      [Setup 모드]
          -> 대화형 설정 모드
          -> running-config,startup-config 파일에 저장
      [전역 설정 모드(=configuration모드)]
          ->CMD 설정 모드
          ->running-config 파일에 저장
      [Interface 설정 모드]
          ->Interface 설정에 사용되는 모드

> 모든간 전환 명령어

![1ccf34aa-76d9-4f1c-a158-9b5ea0edaccd](https://github.com/user-attachments/assets/57c0256d-40cc-405e-8802-9e9a27954962)

<hr>
<hr>

## 기본 명령어

> 모드 진입 명령어

    enable : 특권 모드 전환
    disable : 일반 사용자 모드 전환
    config terminal : 전역설정 모드 전환
    interface 포트라벨:Interface 설정 모드 전환
    exit : 하위 모드로 나가기
    end : 특권 모드로 복귀

<br>

> 라우팅 관련 명령어
    
    show ip route : 라우팅 테이블 확인
    router : 동적 라우팅 프로토콜 사용
    net [NetworkIP] : 동적 라우팅 프로토콜에 네트워크 등록
    show ip protocols : 라우팅 프로토콜 관련 정보 확인
    ip route ~ : 정적 라우팅 프로토콜 설정 

<br>

> 동작 상태 확인 명령어 

    [일반 사용자 모드]
      show clock 
      show history 
      show hosts 
      show sessions 
      show snmp 
      show terminal 
      show users 
      show version 등
      show version 으로 알 수있는 것들
      라우터 타입, IOS image, 시스템 동작시간, 현재 IOS 버젼, 장착된 인터페이스,메모리량 등
    [특권모드]
      show ip interface
      show interface 
      show ip route 
      show running-config
      현재 설정된 상황을 종합적으로 보여줌
      show startup-config







