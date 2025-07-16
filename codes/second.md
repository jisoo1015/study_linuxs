```
#Level 1: 기본 탐색 및 폴더 조작
```

```
PS C:\Develops\temp_dir> pwd

Path
----
C:\Develops\temp_dir


PS C:\Develops\temp_dir> cd C:\Develops\quests\
PS C:\Develops\quests> pwd

Path
----
C:\Develops\quests


PS C:\Develops\quests> mkdir powershell_practice


    디렉터리: C:\Develops\quests


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-07-15   오후 3:36                powershell_practice


PS C:\Develops\quests> cd powershell_practice
PS C:\Develops\quests\powershell_practice> mkdir documents/


    디렉터리: C:\Develops\quests\powershell_practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-07-15   오후 3:38                documents


PS C:\Develops\quests\powershell_practice> mkdir images/


    디렉터리: C:\Develops\quests\powershell_practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-07-15   오후 3:39                images


PS C:\Develops\quests\powershell_practice> mkdir backup/


    디렉터리: C:\Develops\quests\powershell_practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-07-15   오후 3:39                backup


PS C:\Develops\quests\powershell_practice> mkdir temp/


    디렉터리: C:\Develops\quests\powershell_practice


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-07-15   오후 3:39                temp


PS C:\Develops\quests\powershell_practice> tree
폴더 PATH의 목록입니다.
볼륨 일련 번호는 52B6-33C5입니다.
C:.
├─backup
├─documents
├─images
└─temp
PS C:\Develops\quests\powershell_practice> cd ..
PS C:\Develops\quests> tree
폴더 PATH의 목록입니다.
볼륨 일련 번호는 52B6-33C5입니다.
C:.
└─powershell_practice
    ├─backup
    ├─documents
    ├─images
    └─temp
PS C:\Develops\quests> cd documents

PS C:\Develops\quests> cd powershell_practice
PS C:\Develops\quests\powershell_practice> cd documents
PS C:\Develops\quests\powershell_practice\documents> ls
PS C:\Develops\quests\powershell_practice\documents> cd ..
PS C:\Develops\quests\powershell_practice>
```

```
#Level 2: 파일 생성 및 조작
```

```
문제 2-1: 텍스트 파일 생성
PS C:\Develops\quests\powershell_practice\documents> cd ..
PS C:\Develops\quests\powershell_practice> pwd

Path
----
C:\Develops\quests\powershell_practice


PS C:\Develops\quests\powershell_practice> cd documents
```

```
문제 2-2: 파일 내용 확인
PS C:\Develops\quests\powershell_practice\images> ""> New-Item
PS C:\Develops\quests\powershell_practice\images> ls


    디렉터리: C:\Develops\quests\powershell_practice\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2025-07-15   오후 3:58              6 New-Item

PS C:\Develops\quests\powershell_practice\documents> tree
폴더 PATH의 목록입니다.
볼륨 일련 번호는 52B6-33C5입니다.
C:.

에 하위 폴더가 없습니다.
PS C:\Develops\quests\powershell_practice\documents>
```

```
문제 2-3: 파일 복사cd
```

```
Level 3: 파일 이동 및 이름 변경
```

```
문제 3-1: 파일 이동
PS C:\Develops\quests\powershell_practice\documents> cd ..
PS C:\Develops\quests\powershell_practice> cd temp
PS C:\Develops\quests\powershell_practice\temp> "" > test.txt
PS C:\Develops\quests\powershell_practice\temp> ls


    디렉터리: C:\Develops\quests\powershell_practice\temp


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2025-07-15   오후 4:23              6 test.txt


PS C:\Develops\quests\powershell_practice\temp> mv test.txt C:\Develops\quests\powershell_practice\documents
PS C:\Develops\quests\powershell_practice\temp> tree
폴더 PATH의 목록입니다.
볼륨 일련 번호는 52B6-33C5입니다.
C:.
에 하위 폴더가 없습니다.

PS C:\Develops\quests\powershell_practice\temp> cd ..
PS C:\Develops\quests\powershell_practice> cd documents
PS C:\Develops\quests\powershell_practice\documents> ls


    디렉터리: C:\Develops\quests\powershell_practice\documents


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----      2025-07-15   오후 3:52             42 hello.txt
-a----      2025-07-15   오후 4:23              6 test.txt
```
```
문제 3-2: 파일 이름 변경



