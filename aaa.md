권한

drwxr-xr-x 5root root
rwx,r-x,r-x : 소유자,그룹,그 외

사용자 그룹
root root : 허가권
rwxr-xr-x : 소유권

r(Read) 읽기
w(Write) 쓰기
x(eXecute) 실행

|-|문서 | 디렉토리|
|-|-|-|
|r|cat,head,tail,more(내용보기)|ls(목록보기)|
|W|vi (내용수정)|cp,touch,mv.>,rm...(생성,수정,삭제)|
|x|./파일명(실행파일) |cd(진입)|

    r  w  x    
    4  2  1    
    rwxrwxr_x = 775
    421 = 7 421 = 7 401 = 5 775

    123 => __x _w_ _wx

Git 기본 명령어
git init
git add
git commit -m

wd : working directory, sa : staten a--
git reset --soft : commit 취소 wd: o , sa: o
git reset --mixed : commit 취소 wd: o , sa: x
git reset --hard : commit 취소 wd: x, sa: x

Git 병합
git merge
git merge --continue (충돌 해결후 fast - forward merge)
git merge --abort

Git
git branch
git branch [newBranch]
git switch/chekout

git - github연동

git -> github

git
- git init
- git add
- git branch
- git commit -m[message]
- git remote -v
- git remote add orgin githubRepositoy(URL)

github
- new  Repository 생성[README 생성x]

  gitbub -> git
- new  Repository 생성[README 생성o]

git
-git clone URL
-작업
-git push prigin
-git pull origin
git fetch origin







