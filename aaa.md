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
