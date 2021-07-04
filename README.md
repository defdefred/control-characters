# Fun with control characters
Are still control characters used nowdays?
## Few documentation
https://en.wikipedia.org/wiki/Control_character
## Basic file with control characters
```
user@minipc1:~/fred$ od -tu1 test.txt
0000000  48  48  32 104 101 108 108 111   0  32 104 101 108 108 111  10
0000020  48  49  32 104 101 108 108 111   1  32 104 101 108 108 111  10
0000040  48  50  32 104 101 108 108 111   2  32 104 101 108 108 111  10
0000060  48  51  32 104 101 108 108 111   3  32 104 101 108 108 111  10
0000100  48  52  32 104 101 108 108 111   4  32 104 101 108 108 111  10
0000120  48  53  32 104 101 108 108 111   5  32 104 101 108 108 111  10
0000140  48  54  32 104 101 108 108 111   6  32 104 101 108 108 111  10
0000160  48  55  32 104 101 108 108 111   7  32 104 101 108 108 111  10
0000200  48  56  32 104 101 108 108 111   8  32 104 101 108 108 111  10
0000220  48  57  32 104 101 108 108 111   9  32 104 101 108 108 111  10
0000240  49  48  32 104 101 108 108 111  10  32 104 101 108 108 111  10
0000260  49  49  32 104 101 108 108 111  11  32 104 101 108 108 111  10
0000300  49  50  32 104 101 108 108 111  12  32 104 101 108 108 111  10
0000320  49  51  32 104 101 108 108 111  13  32 104 101 108 108 111  10
0000340  49  52  32 104 101 108 108 111  14  32 104 101 108 108 111  10
0000360  49  53  32 104 101 108 108 111  15  32 104 101 108 108 111  10
0000400  49  54  32 104 101 108 108 111  16  32 104 101 108 108 111  10
0000420  49  55  32 104 101 108 108 111  17  32 104 101 108 108 111  10
0000440  49  56  32 104 101 108 108 111  18  32 104 101 108 108 111  10
0000460  49  57  32 104 101 108 108 111  19  32 104 101 108 108 111  10
0000500  50  48  32 104 101 108 108 111  20  32 104 101 108 108 111  10
0000520  50  49  32 104 101 108 108 111  21  32 104 101 108 108 111  10
0000540  50  50  32 104 101 108 108 111  22  32 104 101 108 108 111  10
0000560  50  51  32 104 101 108 108 111  23  32 104 101 108 108 111  10
0000600  50  52  32 104 101 108 108 111  24  32 104 101 108 108 111  10
0000620  50  53  32 104 101 108 108 111  25  32 104 101 108 108 111  10
0000640  50  54  32 104 101 108 108 111  26  32 104 101 108 108 111  10
0000660  50  55  32 104 101 108 108 111  27  32 104 101 108 108 111  10
0000700  50  56  32 104 101 108 108 111  28  32 104 101 108 108 111  10
0000720  50  57  32 104 101 108 108 111  29  32 104 101 108 108 111  10
0000740  51  48  32 104 101 108 108 111  30  32 104 101 108 108 111  10
0000760  51  49  32 104 101 108 108 111  31  32 104 101 108 108 111  10
0001000  49  50  55 104 101 108 108 111 127  32 104 101 108 108 111  10
```
## Same file in bash terminal
```
user@minipc1:~/fred$ cat test.txt
00 hello hello
01 hello hello
02 hello hello
03 hello hello
04 hello hello
05 hello hello
06 hello hello
07 hello hello
08 hell hello
09 hello         hello
10 hello
 hello
11 hello
         hello
12 hello
         hello
 hellolo
14 hello hello
15 hello hello
16 hello hello
17 hello hello
18 hello hello
19 hello hello
20 hello hello
21 hello hello
22 hello hello
23 hello hello
24 hello hello
25 hello hello
26 hello hello
27 hellohello
28 hello hello
29 hello hello
30 hello hello
31 hello hello
127hello hello
```
8 to 13 + 27 seems to be interpreted by bash

## Same file in od -a
```
user@minipc1:~/fred$ od -a test.txt
0000000   0   0  sp   h   e   l   l   o nul  sp   h   e   l   l   o  nl
0000020   0   1  sp   h   e   l   l   o soh  sp   h   e   l   l   o  nl
0000040   0   2  sp   h   e   l   l   o stx  sp   h   e   l   l   o  nl
0000060   0   3  sp   h   e   l   l   o etx  sp   h   e   l   l   o  nl
0000100   0   4  sp   h   e   l   l   o eot  sp   h   e   l   l   o  nl
0000120   0   5  sp   h   e   l   l   o enq  sp   h   e   l   l   o  nl
0000140   0   6  sp   h   e   l   l   o ack  sp   h   e   l   l   o  nl
0000160   0   7  sp   h   e   l   l   o bel  sp   h   e   l   l   o  nl
0000200   0   8  sp   h   e   l   l   o  bs  sp   h   e   l   l   o  nl
0000220   0   9  sp   h   e   l   l   o  ht  sp   h   e   l   l   o  nl
0000240   1   0  sp   h   e   l   l   o  nl  sp   h   e   l   l   o  nl
0000260   1   1  sp   h   e   l   l   o  vt  sp   h   e   l   l   o  nl
0000300   1   2  sp   h   e   l   l   o  ff  sp   h   e   l   l   o  nl
0000320   1   3  sp   h   e   l   l   o  cr  sp   h   e   l   l   o  nl
0000340   1   4  sp   h   e   l   l   o  so  sp   h   e   l   l   o  nl
0000360   1   5  sp   h   e   l   l   o  si  sp   h   e   l   l   o  nl
0000400   1   6  sp   h   e   l   l   o dle  sp   h   e   l   l   o  nl
0000420   1   7  sp   h   e   l   l   o dc1  sp   h   e   l   l   o  nl
0000440   1   8  sp   h   e   l   l   o dc2  sp   h   e   l   l   o  nl
0000460   1   9  sp   h   e   l   l   o dc3  sp   h   e   l   l   o  nl
0000500   2   0  sp   h   e   l   l   o dc4  sp   h   e   l   l   o  nl
0000520   2   1  sp   h   e   l   l   o nak  sp   h   e   l   l   o  nl
0000540   2   2  sp   h   e   l   l   o syn  sp   h   e   l   l   o  nl
0000560   2   3  sp   h   e   l   l   o etb  sp   h   e   l   l   o  nl
0000600   2   4  sp   h   e   l   l   o can  sp   h   e   l   l   o  nl
0000620   2   5  sp   h   e   l   l   o  em  sp   h   e   l   l   o  nl
0000640   2   6  sp   h   e   l   l   o sub  sp   h   e   l   l   o  nl
0000660   2   7  sp   h   e   l   l   o esc  sp   h   e   l   l   o  nl
0000700   2   8  sp   h   e   l   l   o  fs  sp   h   e   l   l   o  nl
0000720   2   9  sp   h   e   l   l   o  gs  sp   h   e   l   l   o  nl
0000740   3   0  sp   h   e   l   l   o  rs  sp   h   e   l   l   o  nl
0000760   3   1  sp   h   e   l   l   o  us  sp   h   e   l   l   o  nl
0001000   1   2   7   h   e   l   l   o del  sp   h   e   l   l   o  nl
```
## Same file in od -c
```
user@minipc1:~/fred$ od -c test.txt
0000000   0   0       h   e   l   l   o  \0       h   e   l   l   o  \n
0000020   0   1       h   e   l   l   o 001       h   e   l   l   o  \n
0000040   0   2       h   e   l   l   o 002       h   e   l   l   o  \n
0000060   0   3       h   e   l   l   o 003       h   e   l   l   o  \n
0000100   0   4       h   e   l   l   o 004       h   e   l   l   o  \n
0000120   0   5       h   e   l   l   o 005       h   e   l   l   o  \n
0000140   0   6       h   e   l   l   o 006       h   e   l   l   o  \n
0000160   0   7       h   e   l   l   o  \a       h   e   l   l   o  \n
0000200   0   8       h   e   l   l   o  \b       h   e   l   l   o  \n
0000220   0   9       h   e   l   l   o  \t       h   e   l   l   o  \n
0000240   1   0       h   e   l   l   o  \n       h   e   l   l   o  \n
0000260   1   1       h   e   l   l   o  \v       h   e   l   l   o  \n
0000300   1   2       h   e   l   l   o  \f       h   e   l   l   o  \n
0000320   1   3       h   e   l   l   o  \r       h   e   l   l   o  \n
0000340   1   4       h   e   l   l   o 016       h   e   l   l   o  \n
0000360   1   5       h   e   l   l   o 017       h   e   l   l   o  \n
0000400   1   6       h   e   l   l   o 020       h   e   l   l   o  \n
0000420   1   7       h   e   l   l   o 021       h   e   l   l   o  \n
0000440   1   8       h   e   l   l   o 022       h   e   l   l   o  \n
0000460   1   9       h   e   l   l   o 023       h   e   l   l   o  \n
0000500   2   0       h   e   l   l   o 024       h   e   l   l   o  \n
0000520   2   1       h   e   l   l   o 025       h   e   l   l   o  \n
0000540   2   2       h   e   l   l   o 026       h   e   l   l   o  \n
0000560   2   3       h   e   l   l   o 027       h   e   l   l   o  \n
0000600   2   4       h   e   l   l   o 030       h   e   l   l   o  \n
0000620   2   5       h   e   l   l   o 031       h   e   l   l   o  \n
0000640   2   6       h   e   l   l   o 032       h   e   l   l   o  \n
0000660   2   7       h   e   l   l   o 033       h   e   l   l   o  \n
0000700   2   8       h   e   l   l   o 034       h   e   l   l   o  \n
0000720   2   9       h   e   l   l   o 035       h   e   l   l   o  \n
0000740   3   0       h   e   l   l   o 036       h   e   l   l   o  \n
0000760   3   1       h   e   l   l   o 037       h   e   l   l   o  \n
0001000   1   2   7   h   e   l   l   o 177       h   e   l   l   o  \n
```
0, 7 to 13 seems to have special meaning for unix.
## Same file in vim
```
00 hello^@ hello↲
01 hello^A hello↲
02 hello^B hello↲
03 hello^C hello↲
04 hello^D hello↲
05 hello^E hello↲
06 hello^F hello↲
07 hello^G hello↲
08 hello^H hello↲
09 hello→→→→→→→→ hello↲
10 hello↲
 hello↲
11 hello^K hello↲
12 hello^L hello↲
13 hello^M hello↲
14 hello^N hello↲
15 hello^O hello↲
16 hello^P hello↲
17 hello^Q hello↲
18 hello^R hello↲
19 hello^S hello↲
20 hello^T hello↲
21 hello^U hello↲
22 hello^V hello↲
23 hello^W hello↲
24 hello^X hello↲
25 hello^Y hello↲
26 hello^Z hello↲
27 hello^[ hello↲
28 hello^\ hello↲
29 hello^] hello↲
30 hello^^ hello↲
31 hello^_ hello↲
127hello^? hello↲
```
Only 9 and 10 are interpreted by vim.
## Same file in Firefox
```
00 hello� hello
01 hello hello
02 hello hello
03 hello hello
04 hello hello
05 hello hello
06 hello hello
07 hello hello
08 hello hello
09 hello	 hello
10 hello
 hello
11 hello hello
12 hello hello
13 hello
 hello
14 hello hello
15 hello hello
16 hello hello
17 hello hello
18 hello hello
19 hello hello
20 hello hello
21 hello hello
22 hello hello
23 hello hello
24 hello hello
25 hello hello
26 hello hello
27 hello hello
28 hello hello
29 hello hello
30 hello hello
31 hello hello
127hello hello
```
0,9,10,13 are interpreted by firefox (try yourself)..
## Same file in less
```
user@minipc1:~/fred$ less test.txt
"test.txt" may be a binary file.  See it anyway?y
00 hello^@ hello
01 hello^A hello
02 hello^B hello
03 hello^C hello
04 hello^D hello
05 hello^E hello
06 hello^F hello
07 hello^G hello
08 hell hello
09 hello         hello
10 hello
 hello
11 hello^K hello
12 hello^L hello
13 hello^M hello
14 hello^N hello
15 hello^O hello
16 hello^P hello
17 hello^Q hello
18 hello^R hello
19 hello^S hello
20 hello^T hello
21 hello^U hello
22 hello^V hello
23 hello^W hello
24 hello^X hello
25 hello^Y hello
26 hello^Z hello
27 helloESC hello
28 hello^\ hello
29 hello^] hello
30 hello^^ hello
31 hello^_ hello
127hello^? hello
```
8-10 and 27 are interpreted by less.
## Same file througth tr
```
user@minipc1:~/fred$ tr "\000-\011,\013-\037,\177" "-" < test.txt
00 hello- hello
01 hello- hello
02 hello- hello
03 hello- hello
04 hello- hello
05 hello- hello
06 hello- hello
07 hello- hello
08 hello- hello
09 hello- hello
10 hello
 hello
11 hello- hello
12 hello- hello
13 hello- hello
14 hello- hello
15 hello- hello
16 hello- hello
17 hello- hello
18 hello- hello
19 hello- hello
20 hello- hello
21 hello- hello
22 hello- hello
23 hello- hello
24 hello- hello
25 hello- hello
26 hello- hello
27 hello- hello
28 hello- hello
29 hello- hello
30 hello- hello
31 hello- hello
127hello- hello
```
All can be catched by tr.
