![image](https://github.com/user-attachments/assets/42c5786d-a235-428a-938c-6a1b0225d88a)# LINUX

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

> mv <br>
* 파일 디렉토리 이동(옵션x)

<br>
<br>

> rm(remove) <br>

* 파일& 디렉토리 삭제 <br>
* 옵션 <br>
  -f : 강제 삭제
  -r : 디렉토리 삭제
  -i : 질의(y/n)

<br>
<br>

> find <br>
* 파일 & 디렉토리 검색
* 옵션
  - name : 파일/디렉토리명 검색
  - perm : 지정된 퍼미션 검색
  - size : 파일 크기가 일치하는 파일 찾기
  - type : 파일 형식 지정함 
  - exec : 검색 결과를 해당 명령어로 실행 하는 옵션
  <br>

  - o	 : 복수 옵션 적용 <br>
  - type : 파일 유형검색 (파일 or 디렉토리) <br>
  
  <br>
  
  - atime n	: n일 전에 엑세스한 파일 찾기, +n 또는 -n 형식으로도 사용가능
  - mtime n	: n일 전에 마지막으로 수정된 파일 찾기, +n 또는 -n 형식으로도 사용가능
  - newer	: 지정된 파일 이후 생성된 파일 찾기
  - used n	: 변경된지 n일이 지난 모든 파일 찾기
  - uid	: 지정된 UID를 가진 파일 검색
  - gid	: 지정된 GID를 가진 파일 검색
  - group	: 지정된 그룹을 가진 파일 검색
  - user	: 지정된 소유자가 소유한 모든 파일 검색



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
