# Third Lab Report - Jun T.

In this lab report, I choose the command `find` and find 4 ways to use it. In example 1 and 2, I use the `-name` option to search for a file in a directory with a specific name. In example 3 and 4, I use the `-type` option to search for files based on their types. In example 5 and 6, I use the `-empty` option to search for files or directories that are empty or have no content. In example 7 and 8, I use the `xargs wc` option to find and count the lines, words, and characters of the files in a given directory.


Example 1:

The command `find technical -name "chapter-2.txt"` will find the file `chapter-2.txt` in technical.

```
(base) JundeAir:docsearch jun.tan.1$ find technical -name "chapter-2.txt"

technical/911report/chapter-2.txt
```
Find it in the [lab report 3 write up](https://ucsd-cse15l-s23.github.io/week/week5/#week5-lab-report).


Example 2:

The command `find technical -name "chapter*.txt"` find all the `txt` files starting with `chapter` in technical.

```
(base) JundeAir:docsearch jun.tan.1$ find technical -name "chapter*.txt"

technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```
Find it in the [lab report 3 write up](https://ucsd-cse15l-s23.github.io/week/week5/#week5-lab-report).


Example 3:

The command line `find technical -type d` find all directories in technical.

```
(base) JundeAir:docsearch jun.tan.1$ find technical -type d

technical
technical/government
technical/government/About_LSC
technical/government/Env_Prot_Agen
technical/government/Alcohol_Problems
technical/government/Gen_Account_Office
technical/government/Post_Rate_Comm
technical/government/Media
technical/plos
technical/biomed
technical/911report
```
Find it in the website [43 Practical Examples of Linux Find Command](https://sysaix.com/43-practical-examples-of-linux-find-command).


Example 4:

The command line `find technical -type f -name "rr*.txt"` find all `txt` files starting with `rr` in the technical directory.

```
(base) JundeAir:docsearch jun.tan.1$ find technical -type f -name "rr*.txt"

technical/biomed/rr73.txt
technical/biomed/rr74.txt
technical/biomed/rr171.txt
technical/biomed/rr167.txt
technical/biomed/rr166.txt
technical/biomed/rr172.txt
technical/biomed/rr37.txt
technical/biomed/rr196.txt
technical/biomed/rr191.txt
```
Find it in the website [43 Practical Examples of Linux Find Command](https://sysaix.com/43-practical-examples-of-linux-find-command).


Example 5:

The command line `find technical/911report -empty` find empty files in the `911report` directory. It turns out that there're no empty files in `911report`.

```
(base) JundeAir:docsearch jun.tan.1$ find technical/911report -empty
```

Find it in the website [How to use find Command in Linux?](https://geekflare.com/how-to-use-find-command-in-linux/).


Example 6:

The command line `find technical/plos -empty` find empty files in the `plos` directory. It turns out that there're no empty files in `plos`.

```
(base) JundeAir:docsearch jun.tan.1$ find technical/plos -empty
```

Find it in the website [How to use find Command in Linux?](https://geekflare.com/how-to-use-find-command-in-linux/).


Example 7:

The command line `find technical/911report |xargs wc` count the lines, words, and characters for each files in the `911report` directory.

```
(base) JundeAir:docsearch jun.tan.1$ find technical/911report |xargs wc

wc: technical/911report: read: Is a directory
    2941   34343  265912 technical/911report/chapter-13.4.txt
    3237   37985  290993 technical/911report/chapter-13.5.txt
    1089   10689   89854 technical/911report/chapter-13.1.txt
    1236   14348  110568 technical/911report/chapter-13.2.txt
    1718   19349  150467 technical/911report/chapter-13.3.txt
    3159   33834  264360 technical/911report/chapter-3.txt
     948   10539   79803 technical/911report/chapter-2.txt
     731   19260  118656 technical/911report/chapter-1.txt
    1204   13004   99008 technical/911report/chapter-5.txt
    1898   19381  149063 technical/911report/chapter-6.txt
    1579   17276  128370 technical/911report/chapter-7.txt
    1885   19748  149644 technical/911report/chapter-9.txt
    1036   11324   84835 technical/911report/chapter-8.txt
     108    1253    9332 technical/911report/preface.txt
    1539   15623  127587 technical/911report/chapter-12.txt
     603    6064   47307 technical/911report/chapter-10.txt
     817    9414   71151 technical/911report/chapter-11.txt
   25728  293434 2236910 total
```

Find it in the website [How to Use the Linux xargs Command](https://phoenixnap.com/kb/xargs-command).
   
   Example 8:
   
   The command line `find technical/government/Media/*Commercial* |xargs wc` count the lines, words, and characters for each files in the `Media` directory that contains the string `Commercial`.
   
```
(base) JundeAir:docsearch jun.tan.1$ find technical/government/Media/*Commercial* |xargs wc

     128    1095    6363 technical/government/Media/CommercialAppealMemphis2.txt
      51     378    2311 technical/government/Media/Commercial_Appeal.txt
     179    1473    8674 total
```


Find it in the website [How to Use the Linux xargs Command](https://phoenixnap.com/kb/xargs-command).
