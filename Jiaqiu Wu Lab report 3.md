## Jiaqiu Wu Lab report3
# Researching Commands

I will find four different command-line options to use the "find" commands.

### find -name:

I think it's useful because `find -name` helps me to find all the files with the pattern I want in a specific folder. For instance, if I want to count the number of files with suffix ".txt" in some folder, I can use this command and redirect the output to another file, then use `wc` command on it.

Example 1:

```
find written_2/non-fiction/OUP/Berk -name "*.txt" 
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch7.txt
```

Find all files with ".txt" suffix in "written_2/non-fiction/OUP/Berk" folder.

Source:[Link to `find -name` command](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line)

Example 2:

```
find written_2 -name "China-History.txt"
written_2/travel_guides/berlitz2/China-History.txt
```

Find all files with the file name "China-History.txt" in the "written_2" folder.

Source:[Link to `find -name` command](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line)


### find -type:

I think it's useful because `find -type f` helps me to find all the files in a specific folder. For instance, if I would like to see the filenames of all the files in some folder, I could use this command, and it will show you the relative paths to those files as well.
And `find -type d` helps me to find all the subfolders in a specific folder. I could use this command to see the names of those subfolders, and the command will show me the paths to those folders too.

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

Source:[Link to `find -type f` command](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line)

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

Find all the subfolders in "written_2" folder.

Source:[Link to `find -type d` command](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line)


### find -mmin:

I think it's useful because `find -mmin` helps me to find all the files modified in a specific folder within the last n(n>=0) minutes. For example, if I modified several files in last 1 hour and I don't remember where they are. I can use this command to find them by setting n = 60.

Example 1:

```
find written_2 -mmin -40
written_2/travel_guides/berlitz2
written_2/travel_guides/berlitz2/California-History.txt
```

Find all files modified within the last 40 minutes in "written_2" folder.

Source:[Link to `find -mmin` command](https://sysaix.com/43-practical-examples-of-linux-find-command)

Example 2:

```
find written_2 -mmin -5
```

Find all files modified within the last 5 minutes in "written_2" folder.

Source:[Link to `find -mmin` command](https://sysaix.com/43-practical-examples-of-linux-find-command)


### find -amin:

I think it's useful because `find -amin` helps me to find all the files I accessed within the last n(n>=0) minutes. For example, if I accessed several files in last 1 hour and I don't remember where they are. I can use this command to find them by setting n = 60.

Example 1:

```
find written_2 -amin -30
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz1/HandRHawaii.txt
```

Find all files accessed within the last 30 minutes in "written_2" folder.

Source:[Link to `find -amin` command](https://geekflare.com/linux-find-commands)

Exmaple 2:

```
find written_2 -amin -5
```

Find all files accessed within the last 5 minutes in "written_2" folder.

Source:[Link to `find -amin` command](https://geekflare.com/linux-find-commands)
