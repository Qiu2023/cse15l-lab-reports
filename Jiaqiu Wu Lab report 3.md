## Jiaqiu Wu Lab report3
# Researching Commands

I will find four different command-line options to use the "find" commands.

### find -name:

Example 1:

```
find written_2/non-fiction/OUP/Berk -name "*.txt" 
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch7.txt
```

Find all files with ".txt" suffix in "written_2/non-fiction/OUP/Berk" folder.\
I think it's useful because it helps me to find all the files with the pattern I want in a specific folder.

Source:[Link](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line)

Example 2:

```
find written_2 -name "China-History.txt"
written_2/travel_guides/berlitz2/China-History.txt
```

Find all files with the file name "China-History.txt" in the "written_2" folder.

Source:[Link](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line)


### find -type:

Example 1:

```
find written_2/non-fiction/OUP/Abernathy -type f
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```

Find all files in "written_2/non-fiction/OUP/Abernathy" folder whose file type is normal file.

Source:[Link](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line)

Example 2:

```
find written_2 -type d                          
written_2
written_2/non-fiction
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Rybczynski
written_2/non-fiction/OUP/Kauffman
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Castro
written_2/travel_guides
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz2
```

Find all the subfolds in "written_2" folder.

Source:[Link](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line)


### find -cmin:

Example 1:

```
find written_2 -cmin -40
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz1/H
```

Find all files created within 40 minutes in "written_2" folder.

Source:[Link](https://sysaix.com/43-practical-examples-of-linux-find-command)

Example 2:

```
find written_2 -cmin -5
```

Find all files created within 5 minutes in "written_2" folder.

Source:[Link](https://sysaix.com/43-practical-examples-of-linux-find-command)


### find -amin:

Example 1:

```
find written_2 -amin -30
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz1/HandRHawaii.txt
```

Find all files accessed within 30 minutes in "written_2" folder.

Source:[Link](https://geekflare.com/linux-find-commands)

Exmaple 2:

```
find written_2 -amin -5
```

Find all files accessed within 5 minutes in "written_2" folder.

Source:[Link](https://geekflare.com/linux-find-commands)
