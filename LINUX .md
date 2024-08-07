# LINUX

> ## LINUX OS 의 특징

1. 무료
2. 오픈소스 - 구조를 볼 수 있다.
3. C언어 -> 플랫폼에 독립적 사용

## 리눅스 명령어

### 01

> 패스워드 변경

    passwd : 접속중인 사용자 패스워드 변경 (최소 6자리 root는 제외)

> 재부팅

    reboot
    shoutdown -r npw
    init 6

<br>

> 종료

    power off
    shutdown -h now
    Halt
    init 0

<br>

### 02

> ifconfig
* 네트워크 확인 명령어
<br>

> pwd(Print Working Directory)
* 현재 위치 확인 명령어
<br>

> cd(Change Directory)
* 디렉토리 변경 명령어
<br>
    
    1. 절대 명령어 /(최상위 디렉토리)가 기준     
        
        
    2. 상대 경로 : 현재 작업중인 디렉토리가 기준 (경로 /home/ 에서 시작) 
             
      1) cd user1 	현재 위치(/home)에서 하위디렉토리 user1 이동 (/home/user1)     
      2) cd .		현재 디렉토리 (/home/user1)     
      3) cd .. 		상위 디렉토리 이동 (/home)      
      4) cd etc		현재 위치에서(/)에서 하위 디렉토리 etc 이동(/etc)     
      5) cd ~		현재 접속중인 사용자의 홈디렉토리로 이동     

<br>

cf) 경로이동에 사용되는 특수문자 <br>
.  : 현재디렉토리 <br>
.. : 상위디렉토리 <br>
~(틸트) : 사용자의 홈디렉토리 <br>
<br>
> **ls(List)**
 * 파일& 디렉토리 목록 출력 <br>
 * 옵션 ex) ls -a /etc -> etc 목록 모든 출력 <br>
   -a : 모두 보기 <br>
   -l : 자세히 보기 <br>
   -r : 하위까지 보기 <br>
   -d : 디렉토리 보기  <br>

   <br>

> **mkdir(Make Directory)** <br>
 * 디렉터리 생성 명령어
 * 옵션 ex) mkdir /home/test -> home 디렉터리에 test 디렉터리 생성 <br>
  -p : 상위디렉토리 포함 생성<br>
<br>

> **man(manual)** <br>
* 명령어 정보 확인 <br>
<br>

> **touch** <br>
 * 파일생성, 파일의 시간을 변경 <br>
 * 옵션  <br>
  -d 12:43 :  (date time) 시간 12:43 변경 <br>
  -t YYYYMMDDHHmmss : 날짜시간변경 <br>
  <br>

> **cp(copy)** <br>
* 파일복사 <br>
* 옵션 <br>
  -i : 질의(믈어보는 것) <br>
  -r : 강제 복사 <br>
  -r : 디렉토리 강제복사 <br>
  -p : 보존 복사 <br>
  
  

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
