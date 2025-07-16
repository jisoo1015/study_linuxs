## 리눅스 상대 주소 실습 문제
사전 준비: 실습 환경 설정
다음 명령어로 실습 환경을 준비하세요:
mkdir -p ~/practice/project/{src,docs,tests,config}
mkdir -p ~/practice/project/src/{main,utils}
mkdir -p ~/practice/project/docs/{user,dev}
mkdir -p ~/practice/project/tests/unit
touch ~/practice/project/README.md
touch ~/practice/project/src/main/app.py
touch ~/practice/project/src/utils/helper.py
touch ~/practice/project/docs/user/manual.txt
touch ~/practice/project/docs/dev/api.md
touch ~/practice/project/tests/test_main.py
touch ~/practice/project/config/settings.conf

완성된 디렉토리 구조:
~/practice/project/
├── README.md
├── src/
│   ├── main/
│   │   └── app.py
│   └── utils/
│       └── helper.py
├── docs/
│   ├── user/
│   │   └── manual.txt
│   └── dev/
│       └── api.md
├── tests/
│   ├── unit/
│   └── test_main.py
└── config/
    └── settings.conf


## 연습문제 1: 기본 상대 주소 이해
1-1. 현재 위치에서 상대 주소 작성
현재 위치가 ~/practice/project/src/main/일 때, 다음 파일들로 이동하는 상대 주소를 작성하시오:

helper.py 파일 
README.md 파일 
manual.txt 파일 
settings.conf 파일 

1-2. 상대 주소 검증
위에서 작성한 상대 주소가 정확한지 다음 명령어로 확인하시오:
cd ~/practice/project/src/main/
```
[kimjisoo@localhost ~]$ cd ~/practice/project/src/main
[kimjisoo@localhost main]$ ls ../utils
helper.py
[kimjisoo@localhost main]$ 
```
```
[kimjisoo@localhost main]$ ls ../../README.md 
../../README.md
[kimjisoo@localhost main]$ 
```
```
[kimjisoo@localhost main]$ ls ../../docs/user/manual.txt
../../docs/user/manual.txt
[kimjisoo@localhost main]$ 
```
```
[kimjisoo@localhost main]$ ls ../../config/settings.conf
../../config/settings.conf
[kimjisoo@localhost main]$ 
```
## 연습문제 2: 다양한 시작점에서의 상대 주소
2-1. 시작점 변경 실습
현재 위치가 ~/practice/project/docs/user/일 때:
app.py 파일로 이동하는 상대 주소를 작성하시오.
```
[kimjisoo@localhost user]$ cd ../../src/main/
[kimjisoo@localhost main]$ 
```
test_main.py 파일을 상대 주소를 작성하시오.
```
[kimjisoo@localhost project]$ cd ~/practice/project/docs/user/
[kimjisoo@localhost user]$ cd ../../tests/
[kimjisoo@localhost tests]$ 
```
src/utils/ 디렉토리로 이동하는 상대 주소를 작성하시오.
```
[kimjisoo@localhost tests]$ cd ~/practice/project/docs/user/
[kimjisoo@localhost user]$ cd ../../src/
[kimjisoo@localhost src]$ 
```

2-2. 역방향 상대 주소
현재 위치가 ~/practice/project/tests/unit/일 때:
프로젝트 루트(~/practice/project/)로 이동하는 상대 주소를 작성하시오.
```
[kimjisoo@localhost src]$ cd ~/practice/project/tests/unit/
[kimjisoo@localhost unit]$ cd ../../
[kimjisoo@localhost project]$
```
api.md 파일로 이동하는 상대 주소를 작성하시오.
```
[kimjisoo@localhost project]$ cd ~/practice/project/tests/unit/
[kimjisoo@localhost unit]$ cd ../../docs/dev
[kimjisoo@localhost dev]$ ls
api.md
```

helper.py 파일을 상대 주소를 작성하시오.
```
[kimjisoo@localhost dev]$ cd ~/practice/project/tests/unit/
[kimjisoo@localhost unit]$ cd ../../src/utils
[kimjisoo@localhost utils]$ ls
helper.py
```


## 연습문제 3: 파일 내용 확인 및 조작
3-1. 상대 주소를 이용한 파일 내용 출력
현재 위치가 ~/practice/project/src/utils/일 때:
프로젝트 루트의 README.md 파일 내용을 출력하시오.
```
[kimjisoo@localhost utils]$ cd ~/practice/project/src/utils/
[kimjisoo@localhost utils]$ cat ../../README.md
[kimjisoo@localhost utils]$ 
```
docs/user/manual.txt 파일 정보 자세히 출력하시오.
```
[kimjisoo@localhost utils]$ ls -l ../../docs/user/manual.txt 
-rw-r--r--. 1 kimjisoo kimjisoo 0 Jul 16 16:23 ../../docs/user/manual.txt
```

config/settings.conf 파일 정보 자세히 출력하시오.
```
[kimjisoo@localhost utils]$ ls -l ../../config/settings.conf
-rw-r--r--. 1 kimjisoo kimjisoo 0 Jul 16 16:24 ../../config/settings.conf
```
3-2. 상대 주소를 이용한 파일 생성
현재 위치가 ~/practice/project/src/main/일 때:
현재 디렉토리에 config.py 파일을 생성하고 "# Configuration module"이라는 내용을 작성하시오.
```
[kimjisoo@localhost utils]$ cd ~/practice/project/src/main/
[kimjisoo@localhost main]$ echo "# Configuration module" > config.py
[kimjisoo@localhost main]$ ls
app.py  config.py
```
tests/ 디렉토리에 test_app.py 파일을 생성하고 "# App test file"이라는 내용을 작성하시오.
```
[kimjisoo@localhost ~]$ cd ~/practice/project/tests/
[kimjisoo@localhost tests]$ echo "# App test file" > test_app.py
[kimjisoo@localhost tests]$ ls
test_app.py  test_main.py  unit
```

연습문제 4: 파일 복사 및 이동
4-1. 상대 주소를 이용한 파일 복사
현재 위치가 ~/practice/project/docs/dev/일 때:

api.md 파일을 docs/user/ 디렉토리에 api_copy.md로 복사하시오.
```
[kimjisoo@localhost dev]$ cp api.md ../../docs/user/api_copy.md 
[kimjisoo@localhost dev]$ ls
api.md
```
src/utils/helper.py 파일을 현재 디렉토리에 복사하시오.
```
[kimjisoo@localhost dev]$ cp ../../src/utils/helper.py ./
[kimjisoo@localhost dev]$ ls
api.md  helper.py
```
config/settings.conf 파일을 tests/unit/ 디렉토리에 복사하시오.
```
[kimjisoo@localhost dev]$ cp ../../config/settings.conf ../../tests/unit
[kimjisoo@localhost dev]$ cd ../../tests/unit/
[kimjisoo@localhost unit]$ ls
settings.conf
```
4-2. 상대 주소를 이용한 파일 이동
현재 위치가 ~/practice/project/tests/일 때:
test_main.py 파일을 tests/unit/ 디렉토리로 이동하시오.
```
[kimjisoo@localhost tests]$ mv test_main.py unit
[kimjisoo@localhost tests]$ ls
test_app.py  unit
```
src/main/config.py 파일을 config/ 디렉토리로 이동하시오.
```
[kimjisoo@localhost tests]$ cd ~/practice/project/tests/
[kimjisoo@localhost tests]$ mv ../src/main/config.py ../config/
```

연습문제 5: 복합 상대 주소 활용
5-1. 다중 파일 조작
현재 위치가 ~/practice/project/일 때:
src/main/ 디렉토리의 모든 파일을 docs/dev/ 디렉토리에 복사하시오.
```
[kimjisoo@localhost project]$ cp ./src/main/app.py ./docs/dev/ 
```
docs/user/ 디렉토리의 모든 파일을 tests/unit/ 디렉토리로 이동하시오.
```
[kimjisoo@localhost project]$ cp .docs/user/{api_copy.md,manual.txt} ./tests/units/
```
config/ 디렉토리 전체를 backup_config/로 복사하시오.
```
[kimjisoo@localhost project]$ cp -r ./config/ ./backup_config/
```



연습문제 6: 에러 찾기 및 수정
6-1. 잘못된 상대 주소 찾기
현재 위치가 ~/practice/project/docs/user/일 때, 다음 명령어들 중 에러가 있는 것을 찾고 올바른 명령어로 수정하시오:
# A
ls ../../../project/src/main/
에러없음

# B
cat ../../src/utils/helper.py
에러없음

# C
cd ../dev/../../config/
에러없음

# D
cp manual.txt ../../tests/unit/backup.txt
```
cp: cannot stat 'manual.txt': No such file or directory
```


# E
mv api_copy.md ../../../src/main/
```
mv: cannot stat 'api_copy.md': No such file or directory
```

6-2. 경로 최적화
다음 상대 주소를 더 간단하게 최적화하시오:
현재 위치: ~/practice/project/tests/unit/
../../src/main/../utils/helper.py
../../docs/user/../dev/api.md
../../config/../README.md

연습문제 7: 종합 실습
7-1. 프로젝트 구조 재정리
현재 위치가 ~/practice/project/일 때, 다음 작업을 수행하시오:
src/main/ 디렉토리에 models/ 하위 디렉토리를 생성하시오.
docs/ 디렉토리에 README.md 파일을 생성하고 "# Project Documentation"이라는 내용을 작성하시오.
tests/unit/ 디렉토리의 모든 파일을 tests/ 디렉토리로 이동하시오.
config/ 디렉토리의 모든 파일을 src/ 디렉토리에 복사하시오.
7-2. 백업 및 정리
현재 위치가 ~/practice/project/src/main/일 때:
전체 프로젝트를 ../../project_backup/으로 복사하시오.
utils/ 디렉토리의 모든 .py 파일을 현재 디렉토리의 models/ 디렉토리로 복사하시오.
프로젝트 루트의 README.md 파일을 현재 디렉토리에 PROJECT_INFO.md로 복사하시오.
