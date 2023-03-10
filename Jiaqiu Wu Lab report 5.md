## Jiaqiu Wu Lab report5

I would like to further explore on several options of a different command for lab report 3.

I will find four different command-line options to use the "grep" commands.

### grep -w

I think it's useful because it can be used to match an exact word in a file, showing the exact occurrences of a word rather than just the occurrence of a pattern. Since `grep -w` will force pattern to match only whole words.

Example 1:

```
grep -w "History" HistoryHongKong.txt 
        A Brief History
```

Find the exact matches of "History" in the file "HistoryHongKong.txt".

Example 2:

```
grep -w "Tang" HistoryHongKong.txt
        incomers, the “Five Great Clans”: Tang, Hau, Pang, Liu, and Man. First
        to arrive was the Tang clan, which established a number of walled
        Adjacent to Lo Wai is the Tang Chung Ling Ancestral Hall, built in the
```

Find the exact matches of "Tang" in the file "HistoryHongKong.txt".

Source:[Link to `grep -w` command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)

### grep -c:

I think it's useful because it can be used to count the number of times the matched string appears in the file. The -c flag can be very useful if you have to count the number of times an error message appeared in a log file.

Example 1:

```
grep -c "China" HistoryHongKong.txt 
19
```

Example 2:

```
grep -c "America" WhatToLosAngeles.txt 
2
```

Source:[Link to `grep -w` command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)

### grep -r:

Example 1:

Example 2:

### grep -l

Example 1:

Example 2:
