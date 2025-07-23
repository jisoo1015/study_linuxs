# 인자와 read를 함께 사용하여 변수 조합 출력

~$ 80_2_shell_variables_read.sh agument_first
 read input : read_first

input values : agument_first read_first

```shell
#nano에 입력:                                         
agument_first="$1"

read -p "input: " read_first

echo "$agument_first,$read_first"
```
```shell
#결과:
[kimjisoo@localhost Downloads]$ source 80_2_shell_variables_read.sh haha
input: hello
haha,hello
```

