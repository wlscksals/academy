# LINUX

## SERVER / CLIENT

|CLIENT|SERVER|SERVICE|NETWORK|
|-|-|-|-|
|서비스 '이용' 주체|서비스 '제공' 주체|클라이언트의 욕구를 만족시키는 것들(프로그램's)|서버와 클라이언트를 연결|
|사람|고기집|항정살/가브리살/목살..|홀서빙직원|
|웹브라우저|서버컴퓨터(장치)|서비스 프로그램|인터넷|
<br>
<br>

## OS

**Program** : 사전에 해야 '할일' 들을 '순서'대로 적은 목록 <br>
**Software** : 기계(ex)가 해야할 일들을 저장한 프로그램 <br>
**Hardware** : Software가 특정 역할수행에 필요한 물리적인 자원들(연산장치,보조기억장치,주기억장치..)
<br>
<br>

> Operating System(OS)

* **운영 체제** <br>

      컴퓨터나 다른 디지털 장치에서 소프트웨어와 하드웨어 간의 상호 작용을 관리하고 제어하는 '시스템 소프트웨어' 이는 사용자와 하드웨어 사이의 인터페이스 역할을 하며, 응용 프로그램이 하드웨어 자원(예: CPU, 메모리, 저장 장치 등)을 사용할 수 있도록 함

<br>

* **Application** <br>

      운영제체에 의해 자원을 할당받아 사용자의 목적에 맞는 일처리를 도와주는 응용프로그램      

## 다운로드

ORCLE VM 설치 - https://phantom.tistory.com/6 <br>
UBUNT ISO 설치 - https://ubuntu.com/download/desktop <br>
UBUNT VM 설치 - https://mainia.tistory.com/2379 <br>



Ubuntu에서 SSH 설정

1. Ubuntu 시스템에서 SSH를 설치
   1) Ctrl + Alt+ T로 터미널을 연다.
   2) openssh-server 패키지를 설치
      - sudo apt update
      - sudo apt install openssh-server 입력
      - sudo systemctl status ssh 설치확인하기
   3) SSH 서버연결
      - ssh username@ip_address 사용자 이름 및 IP 주소를 다음 형식으로 호출 ex) ssh jjeongil@10.0.2.15
      ※ ip 주로를 모를 경우 ip a 를 입력
   4)  NAT 지원 SSH 연결
      





1. repo update
   sudo apt update

apt 레파지토를 받거나 지우거나 할때 사용
sudo - 계정 전환
관리자 권한 을 잠깐 습득해서 실행한다.

sudo apt install openssh - server
2. ssh Service install - 원격조정

3. 설치 확인
sudo apt systemctl status ssh

putty 설치

sudo su


LINUX OS 의 특징
<br>

1. 무료
2. 오픈소스 - 구조를 볼 수 있다.
3. C언어 -> 플랫폼에 독립적 사용

리눅스 여러개 파일 복사

VI  설치 - 메모장 기능
apt installl vim

기본 명령어
passwd
ifconfig
pwd 현재 위치
cd 위치변경
ls 디렉토리 목록 확인
mkdir 폴더 만들기 
touch 파일 만들기
cp 파일 복사
mv 이동
rm 삭제
--
head
tail
more
> 파일 저장
< 파일 불러오기
vi ex) 매모장
