# Linux 실습 문제지 - nano, 쉘 스크립트, 다중 명령어, chmod
## 기본 개념 정리
```
nano 편집기
nano : 터미널 기반 텍스트 편집기
Ctrl+X : 편집기 종료
Ctrl+O : 파일 저장
Ctrl+K : 현재 줄 잘라내기
Ctrl+U : 잘라낸 텍스트 붙여넣기
권한 부여
Chmod 777 대상_파일명
```
Linux 명령어 실습 문제
nano 편집기, 실행 쉘 작성, && 연산자 활용
실습 환경 설정
먼저 다음 명령어를 실행하여 실습 환경을 만들어보세요:
```
mkdir shell_practice
cd shell_practice
touch data.txt config.conf notes.md
mkdir scripts logs backup
```

## 문제 1: nano 편집기 활용
### 1-1. 간단한 설정 파일 생성
nano 편집기를 사용하여 server.conf 파일을 생성하고 다음 내용을 입력하세요:
PORT=8080
HOST=localhost
DEBUG=true
```
명령어를 작성하세요
[kimjisoo@localhost shell_practice]$ nano server.conf
```
### 1-2. 기존 파일 수정
nano 편집기로 data.txt 파일을 열어서 "Hello Linux World!" 텍스트를 추가하세요.
```
명령어를 작성하세요
[kimjisoo@localhost shell_practice]$ nano data.txt
```

## 문제 2: 실행 가능한 쉘 스크립트 작성
### 2-1. 백업 스크립트 생성
backup.sh 파일을 생성하여 다음 기능을 수행하는 스크립트를 작성하세요:
현재 날짜와 시간 출력
data.txt 파일을 backup 디렉토리에 복사
복사 완료 메시지 출력 (ls-l)
스크립트 파일 생성 및 실행 권한 부여 명령어를 작성하세요
```
backup.sh에 작성한 내용:
date
cp data.txt ./backup/
./backup.sh (파일실행시키기)
```
```shell
[kimjisoo@localhost shell_practice]$ nano backup.sh
[kimjisoo@localhost shell_practice]$ ./backup.sh
bash: ./backup.sh: Permission denied
[kimjisoo@localhost shell_practice]$ chmod 777 ./backup.sh (권한부여)
[kimjisoo@localhost shell_practice]$ ./backup.sh
Fri Jul 18 03:03:11 PM KST 2025
total 4
-rw-r--r--. 1 kimjisoo kimjisoo 20 Jul 18 15:03 data.txt

```

### 2-2. 시스템 정보 출력 스크립트
sysinfo.sh 스크립트를 생성하여 현재 사용자명(whoami), 현재 디렉토리(pwd), 디스크 사용량(df -을 출력하는 스크립트를 작성하고 실행하세요.
명령어를 작성하세요
```
[kimjisoo@localhost shell_practice]$ nano sysinfo.sh

```
nano에 작성한 스크립트
```
hoami
pwd
df -h
```
```
[kimjisoo@localhost shell_practice]$ ./sysinfo.sh (파일 실행)
bash: ./sysinfo.sh: Permission denied (권한 없음)
[kimjisoo@localhost shell_practice]$ chmod 777 ./sysinfo.sh  (권한부여)
[kimjisoo@localhost shell_practice]$ ./sysinfo.sh (다시 파일실행)
kimjisoo
/home/kimjisoo/quests/shell_practice
Filesystem           Size  Used Avail Use% Mounted on
devtmpfs             4.0M     0  4.0M   0% /dev
tmpfs                870M     0  870M   0% /dev/shm
tmpfs                348M  7.2M  341M   3% /run
/dev/mapper/rl-root   17G  5.7G   12G  34% /
/dev/nvme0n1p1       960M  366M  595M  39% /boot
tmpfs                174M  112K  174M   1% /run/user/1000
/dev/sr0              12G   12G     0 100% /run/media/kimjisoo/Rocky-9-6-x86_64-dvd
```
## 문제 3: && 연산자를 이용한 다중 명령어 실행
### 3-1. 디렉토리 생성과 파일 생성
projects 디렉토리를 생성하고, 성공하면 그 안에 readme.txt 파일을 생성하는 한 줄 명령어를 작성하세요.
명령어를 작성하세요
```shell
&& 엠퍼서트 사용
[kimjisoo@localhost shell_practice]$ mkdir projects && touch ./projects/readme.txt
```
```
[kimjisoo@localhost shell_practice]$ mkdir -p projects/readme.txt
```
### 3-2. 파일 존재 확인과 내용 출력
server.conf 파일이 존재하는지 확인하고, 존재하면 파일 내용을 출력하는 한 줄 명령어를 작성하세요.
명령어를 작성하세요
```
[kimjisoo@localhost shell_practice]$ ls server.conf && cat server.conf 
server.conf
PORT=8080
HOST=localhost
DEBUG=true
```
### 3-3. 복합 작업 실행
다음 작업을 && 연산자로 연결하여 한 줄로 실행하세요:
logs 디렉토리로 이동
access.log 파일 생성
현재 디렉토리 내용 출력
상위 디렉토리로 복귀
```
[kimjisoo@localhost quests]$ cd ./shell_practice/logs && touch ./access.log && ls ./ && cd ../
access.log
```



