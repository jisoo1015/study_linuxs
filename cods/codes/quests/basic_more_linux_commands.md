연습문제 1: 기본 파일 시스템 탐색
1-1. 현재 위치 확인 및 이동
현재 작업 디렉터pw리의 절대 경로를 출력하시오.
홈 디렉터리로 이동하시오.
루트 디렉터리(/)로 이동하시오.
다시 홈 디렉터리로 돌아가시오.
```
[kimjisoo@localhost ~]$ pwd
/home/kimjisoo
[kimjisoo@localhost ~]$ cd ~
[kimjisoo@localhost ~]$ cd /
[kimjisoo@localhost /]$ 
```

1-2. 디렉터리 내용 확인
현재 디렉터리의 파일과 폴더 목록을 출력하시오.
숨김 파일을 포함한 모든 파일의 상세 정보를 출력하시오.
/etc 디렉터리의 내용을 확인하시오.
```
[kimjisoo@localhost /]$ ls
afs  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
[kimjisoo@localhost /]$ ls -al
total 24
dr-xr-xr-x.  18 root root  235 Jul 16 10:33 .
dr-xr-xr-x.  18 root root  235 Jul 16 10:33 ..
dr-xr-xr-x.   2 root root    6 Nov  3  2024 afs
lrwxrwxrwx.   1 root root    7 Nov  3  2024 bin -> usr/bin
dr-xr-xr-x.   5 root root 4096 Jul 16 10:52 boot
drwxr-xr-x.  20 root root 3420 Jul 16 10:52 dev
drwxr-xr-x. 131 root root 8192 Jul 16 10:53 etc
drwxr-xr-x.   3 root root   22 Jul 16 10:53 home
lrwxrwxrwx.   1 root root    7 Nov  3  2024 lib -> usr/lib
lrwxrwxrwx.   1 root root    9 Nov  3  2024 lib64 -> usr/lib64
drwxr-xr-x.   2 root root    6 Nov  3  2024 media
drwxr-xr-x.   3 root root   18 Jul 16 10:34 mnt
drwxr-xr-x.   2 root root    6 Nov  3  2024 opt
dr-xr-xr-x. 312 root root    0 Jul 16 10:52 proc
dr-xr-x---.   4 root root  140 Jul 16 10:52 root
drwxr-xr-x.  47 root root 1240 Jul 16 10:57 run
lrwxrwxrwx.   1 root root    8 Nov  3  2024 sbin -> usr/sbin
drwxr-xr-x.   2 root root    6 Nov  3  2024 srv
dr-xr-xr-x.  13 root root    0 Jul 16 10:52 sys
drwxrwxrwt.  19 root root 4096 Jul 16 10:56 tmp
drwxr-xr-x.  12 root root  144 Jul 16 10:33 usr
drwxr-xr-x.  20 root root 4096 Jul 16 10:52 var
[kimjisoo@localhost /]$ ls /etc
accountsservice          dnsmasq.conf   keyutils                  PackageKit              skel
adjtime                  dnsmasq.d      krb5.conf                 pam.d                   smartmontools
aliases                  dracut.conf    krb5.conf.d               papersize               sos
alsa                     dracut.conf.d  ld.so.cache               passwd                  speech-dispatcher
alternatives             egl            ld.so.conf                passwd-                 ssh
anacrontab               enscript.cfg   ld.so.conf.d              pbm2ppa.conf            ssl
appstream.conf           environment    libaudit.conf             pinforc                 sssd
asound.conf              ethertypes     libblockdev               pkcs11                  statetab.d
at.deny                  exports        libibverbs.d              pkgconfig               subgid
audit                    favicon.png    libnl                     pki                     subgid-
authselect               filesystems    libpaper.d                plymouth                subuid
avahi                    firefox        libreport                 pm                      subuid-
bash_completion.d        firewalld      libssh                    pnm2ppa.conf            sudo.conf
bashrc                   flatpak        libuser.conf              polkit-1                sudoers
bindresvport.blacklist   fonts          locale.conf               popt.d                  sudoers.d
binfmt.d                 foomatic       localtime                 printcap                sudo-ldap.conf
bluetooth                fprintd.conf   login.defs                profile                 sysconfig
brlapi.key               fstab          logrotate.conf            profile.d               sysctl.conf
brltty                   fuse.conf      logrotate.d               protocols               sysctl.d
brltty.conf              fwupd          lsm                       pulse                   systemd
chromium                 gcrypt         lvm                       qemu-ga                 system-release
chrony.conf              gdm            machine-id                ras                     system-release-cpe
chrony.keys              geoclue        magic                     rc.d                    terminfo
cifs-utils               glvnd          mailcap                   rc.local                tmpfiles.d
cockpit                  gnupg          makedumpfile.conf.sample  redhat-release          tpm2-tss
containers               GREP_COLORS    man_db.conf               request-key.conf        trusted-key.key
cron.d                   groff          mcelog                    request-key.d           tuned
cron.daily               group          microcode_ctl             resolv.conf             udev
cron.deny                group-         mime.types                rocky-release           udisks2
cron.hourly              grub2.cfg      mke2fs.conf               rocky-release-upstream  updatedb.conf
cron.monthly             grub.d         modprobe.d                rpc                     UPower
crontab                  gshadow        modules-load.d            rpm                     usb_modeswitch.conf
cron.weekly              gshadow-       motd                      rsyncd.conf             vconsole.conf
crypto-policies          gss            motd.d                    rsyslog.conf            vimrc
crypttab                 host.conf      mtab                      rsyslog.d               virc
csh.cshrc                hostname       multipath                 rwtab.d                 vmware-tools
csh.login                hosts          nanorc                    samba                   vulkan
cups                     hp             netconfig                 sane.d                  wgetrc
cupshelpers              inittab        NetworkManager            sasl2                   wireplumber
dbus-1                   inputrc        networks                  security                wpa_supplicant
dconf                    iscsi          nftables                  selinux                 X11
debuginfod               issue          nsswitch.conf             services                xattr.conf
default                  issue.d        nsswitch.conf.bak         sestatus.conf           xdg
depmod.d                 issue.net      nvme                      setroubleshoot          xml
dhcp                     kdump          openldap                  sgml                    yum
DIR_COLORS               kdump.conf     opt                       shadow                  yum.conf
DIR_COLORS.lightbgcolor  kernel         os-release                shadow-                 yum.repos.d
dnf                      keys           ostree                    shells
```

연습문제 2: 디렉터리 및 파일 생성
2-1. 디렉터리 구조 생성
다음과 같은 디렉터리 구조를 생성하시오:
practice/
├── documents/
│   ├── reports/ls
│   └── notes/
├── images/
└── backup/
```
[kimjisoo@localhost practice]$ cd ..
[kimjisoo@localhost ~]$ cd practice/
[kimjisoo@localhost practice]$ mkdir documents
[kimjisoo@localhost practice]$ mkdir report/ls
mkdir: cannot create directory ‘report/ls’: No such file or directory
[kimjisoo@localhost practice]$ cd ..
[kimjisoo@localhost ~]$ cd documents
bash: cd: documents: No such file or directory
[kimjisoo@localhost ~]$ cd ~
[kimjisoo@localhost ~]$ cd practice
[kimjisoo@localhost practice]$ cd documents
[kimjisoo@localhost documents]$ mkdir reports /ls
mkdir: cannot create directory ‘/ls’: Permission denied
[kimjisoo@localhost documents]$ mkdir reports/ls
[kimjisoo@localhost documents]$ mkdir notes/
[kimjisoo@localhost documents]$ ls
notes  reports
[kimjisoo@localhost documents]$ cd ~
[kimjisoo@localhost ~]$ cd practice
[kimjisoo@localhost practice]$ mkdir images/
[kimjisoo@localhost practice]$ mkdir backup/
[kimjisoo@localhost practice]$ tree
.
├── backup
├── documents
│   ├── notes
│   └── reports
│       └── ls
└── images
```

2-2. 파일 생성 및 내용 작성
practice/documents/ 디렉터리에 readme.txt 파일을 생성하고 "Hello Linux!"라는 내용을 작성하시오.
practice/notes/ 디렉터리에 memo.txt 파일을 생성하고 "Linux 명령어 연습 중"이라는 내용을 작성하시오.
```
[kimjisoo@localhost practice]$ cd ~
[kimjisoo@localhost ~]$ cd practice
[kimjisoo@localhost practice]$ cd documents
[kimjisoo@localhost documents]$ touch readme.txt
[kimjisoo@localhost documents]$ cd ~
[kimjisoo@localhost ~]$ cd practice
[kimjisoo@localhost practice]$ cd notes
bash: cd: notes: No such file or directory
[kimjisoo@localhost practice]$ cd documents
[kimjisoo@localhost documents]$ touch memo.txt
[kimjisoo@localhost documents]$ ls
memo.txt  notes  readme.txt  reports
```

연습문제 3: 파일 내용 확인 및 조작
3-1. 파일 내용 출력
앞서 생성한 readme.txt 파일의 내용을 출력하시오.
memo.txt 파일의 내용을 출력하시오.
```
[kimjisoo@localhost documents]$ cd ~
[kimjisoo@localhost ~]$ cat practice/documents/readme.txt
[kimjisoo@localhost notes]$ cat /home/kimjisoo/practice/documents/notes
cat: /home/kimjisoo/practice/documents/notes: Is a directory
[kimjisoo@localhost notes]$ cat /home/kimjisoo/practice/documents/notes/memo.txt
```
3-2. 파일 복사
readme.txt 파일을 backup/ 디렉터리에 복사하시오.
documents/ 디렉터리 전체를 backup/ 디렉터리에 복사하시오.
```
[kimjisoo@localhost practice]$ cd documents/
[kimjisoo@localhost documents]$ ls
notes  readme.txt  reports
[kimjisoo@localhost documents]$ cp readme.txt /home/kimjisoo/practice/backup
[kimjisoo@localhost documents]$ ls
notes  readme.txt  reports
[kimjisoo@localhost documents]$ cd ..
[kimjisoo@localhost practice]$ cd backup
[kimjisoo@localhost backup]$ ls
readme.txt

[kimjisoo@localhost practice]$ cp -r documents /home/kimjisoo/practice/backup
[kimjisoo@localhost practice]$ tree
.
├── backup
│   ├── documents
│   │   ├── notes
│   │   │   └── memo.txt
│   │   ├── readme.txt
│   │   └── reports
│   │       └── ls
│   └── readme.txt
├── documents
│   ├── notes
│   │   └── memo.txt
│   ├── readme.txt
│   └── reports
│       └── ls
└── images
```


연습문제 4: 파일 이동 및 이름 변경
4-1. 파일 이동
memo.txt 파일을 documents/ 디렉터리로 이동하시오.
images/ 디렉터리를 practice/media/로 이름을 변경하시오.
```
kimjisoo@localhost documents]$ cd ~
[kimjisoo@localhost ~]$ cd practice
[kimjisoo@localhost practice]$ cd documents/notes
[kimjisoo@localhost notes]$ mv memo.txt /home/kimjisoo/practice/documents

[kimjisoo@localhost notes]$ cd ~
[kimjisoo@localhost ~]$ cd practice
[kimjisoo@localhost practice]$ mv images media
[kimjisoo@localhost practice]$ ls
backup  documents  media
```

4-2. 파일 이름 변경
readme.txt를 introduction.txt로 이름을 변경하시오.
memo.txt를 study_notes.txt로 이름을 변경하시오.
```
[kimjisoo@localhost ~]$ cd practice
[kimjisoo@localhost practice]$ cd documents
[kimjisoo@localhost documents]$ mv readme.txt introduction.txt
[kimjisoo@localhost documents]$ mv memo.txt study_notes.txt
[kimjisoo@localhost documents]$ ls
introduction.txt  notes  reports  study_notes.txt
```


연습문제 5: 종합 실습
5-1. 프로젝트 디렉터리 생성
다음 요구사항에 따라 프로젝트 디렉터리를 생성하시오:
my_project/라는 최상위 디렉터리 생성
하위에 src/, docs/, tests/, config/ 디렉터리 생성
src/ 디렉터리에 main.py 파일 생성 (내용: "# Main Python File")
docs/ 디렉터리에 README.md 파일 생성 (내용: "# My Project Documentation")
config/ 디렉터리에 settings.conf 파일 생성 (내용: "# Configuration File")
```
[kimjisoo@localhost my_project]$ cd src/
[kimjisoo@localhost src]$ touch main.py
[kimjisoo@localhost src]$ cd ..
[kimjisoo@localhost my_project]$ cd docs/
[kimjisoo@localhost docs]$ touch README.md
[kimjisoo@localhost docs]$ cd ..
[kimjisoo@localhost my_project]$ cd config/
[kimjisoo@localhost config]$ touch settings.cong
[kimjisoo@localhost config]$ cd ..
[kimjisoo@localhost my_project]$ tree
.
├── config
│   └── settings.cong
├── docs
│   └── README.md
├── src
│   └── main.py
└── tests
```

5-2. 백업 및 정리
전체 my_project/ 디렉터리를 my_project_backup/으로 복사하시오.
my_project/src/main.py 파일을 my_project/src/app.py로 이름을 변경하시오.
my_project/docs/README.md 파일을 my_project/ 디렉터리로 이동하시오.
```

[kimjisoo@localhost my_project]$ cd ..
[kimjisoo@localhost ~]$ cp my_project /home/kimjisoo/my_project/backup
cp: -r not specified; omitting directory 'my_project'
[kimjisoo@localhost ~]$ cp -r  my_project /home/kimjisoo/my_project/backup
cp: cannot copy a directory, 'my_project', into itself, '/home/kimjisoo/my_project/backup/my_project'
[kimjisoo@localhost ~]$ cd ~
[kimjisoo@localhost ~]$ cd /home/kimjisoo/
[kimjisoo@localhost ~]$ mkdir my_project_backup/
[kimjisoo@localhost ~]$ cp -r /home/kimjisoo/my_project/* /home/kimjisoo/my_project_backup
[kimjisoo@localhost ~]$ cd my_project
[kimjisoo@localhost my_project]$ cd src
[kimjisoo@localhost src]$ mv main.py app.py
[kimjisoo@localhost src]$ cd ..
[kimjisoo@localhost my_project]$ cd docs
[kimjisoo@localhost docs]$ mv README.md /home/kimjisoo/my_project
```
