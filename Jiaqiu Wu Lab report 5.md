## Jiaqiu Wu Lab report 5

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

Source:[Link to `grep -w` command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)

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

Count the number of times "China" appears in the file "HistoryHongKong.txt".

Source:[Link to `grep -c` command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)

Example 2:

```
grep -c "America" WhatToLosAngeles.txt 
2
```

Count the number of times "America" appears in the file "WhatToLosAngeles.txt"

Source:[Link to `grep -c` command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)


### grep -r:

This command is very useful because it is used to search for matches of certain character pattern through files recursively from subdirectories, starting from the current directory. 

Example 1:

```
grep -r "Pyramid"                                                                                  
./HistoryEgypt.txt:        the world was graced by the Great Pyramid at Giza built for Khufu (or
./WhereToEgypt.txt:        Cairo and the Pyramids
./WhereToEgypt.txt:        The Pyramids
./WhereToEgypt.txt:        Whatever the latest theory, the Pyramids of Giza (the most
./WhereToEgypt.txt:        robbers. The largest of the three, the Great Pyramid of Cheops is the
./WhereToEgypt.txt:        The Pyramid of Kephren is smaller than the Great Pyramid,
./WhereToEgypt.txt:        place at the site is taken by the Step Pyramid built by architect
./WhereToDublin.txt:        Pyramids (3000 b.c. ). It’s a huge stone mound (nearly 12 m/40 ft high
```

Recursively search for "Pyramid" though files from subdirectories, starting from the current directory "berlitz1".

Source:[Link to `grep -r` command](https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/)

Example 2:

```
grep -r "butterfly"
./non-fiction/OUP/Kauffman/ch1.txt:But life uses mutation, recombination, and selection. These search procedures seem to be working quite well. Your typical bat or butterfly has managed to get itself evolved and seems a rather impressive entity. The no-free-lunch theorem brings into high relief the puzzle. If mutation, recombination, and selection only work well on certain kinds of fitness landscapes, yet most organisms are sexual, and hence use recombination, and all organisms use mutation as a search mechanism, where did these well-wrought fitness landscapes come from, such that evolution manages to produce the fancy stuV around us?
./non-fiction/OUP/Kauffman/ch8.txt:These huge avalanches are exactly the signature of the famous “butterfly eect” seen in the weather, where a small initial change can have large-scale consequences. In short, the spreading purple avalanches constitute “sensitivity to initial conditions.” On the other hand, it is important to distinguish between low-dimensional chaos, characterized by three or four variables governed by three or four equations, and the high-dimensional chaos, shown in large-model genetic networks with tens of thousands of gene variables. In high-dimensional networks of genes modeled as binary variables, chaos shows up as the enormous avalanches of damage that spread from one to many of the variables of the model network.
./travel_guides/berlitz1/WhereToMalaysia.txt:        280 species of butterfly. Bird-life includes stork-billed kingfishers,
./travel_guides/berlitz1/WhereToFWI.txt:        resembles a butterfly.
./travel_guides/berlitz2/Nepal-WhereToGo.txt:Godavari’s Royal Botanical Gardens at the foot of the mountain has an orchid collection, lovely trees, and a brook. It is a favorite haunt of bulbuls, babblers, and minivets, as well as those who understand this language — bird-watchers. A hundred species of butterfly have been identified here, and as many different birds.
./travel_guides/berlitz2/Cancun-WhereToGo.txt:When Xcaret opened in 1990, the cenote and its outlet to the sea (a mixture of narrow gorge and underground tunnel) were the focus of the park; they made an exciting snorkeling or swimming tour. Today this is still a popular attraction, but the park has grown to include sheltered swimming, a beautiful beach, restaurants, tropical gardens, horseback-riding trails, a magnificent butterfly pavilion, a zoo, an aquarium, and a “swim with the dolphins” program. The park is also contributing to a number of projects protecting endangered plants and animals including the green turtle and several parrot species. As night falls, Xcaret holds a number of “spectaculars” which are both entertaining and educational. Mayan rituals are re-enacted at the ancient sites, and a folkloric ballet offers traditional dances from different regions in Mexico.
```

Recursively search for "butterfly" though files from subdirectories, starting from the current directory "written_2".

Source:[Link to `grep -r` command](https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/)


### grep -l

It is useful because we can use this command to find files that contain the provided matching pattern in the current direcoty. This command prints the name of the files where the pattern is found.

Example 1:

```
grep -l "Egypt" *
HistoryEgypt.txt
HistoryFrance.txt
HistoryGreek.txt
HistoryHawaii.txt
HistoryIsrael.txt
HistoryIstanbul.txt
HistoryJerusalem.txt
IntroEgypt.txt
IntroLasVegas.txt
WhatToEgypt.txt
WhereToDublin.txt
WhereToEdinburgh.txt
WhereToEgypt.txt
WhereToFrance.txt
WhereToGreek.txt
WhereToIsrael.txt
WhereToIstanbul.txt
WhereToItaly.txt
WhereToJapan.txt
WhereToJerusalem.txt
WhereToLosAngeles.txt
WhereToMadeira.txt
WhereToMadrid.txt
```

Print the name of the files that contain "Egypt" in the current directory "berlitz1".

Source:[Link to `grep -l` command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)

Example 2:

```
grep -l "romance" * 
WhereToIndia.txt
WhereToItaly.txt
WhereToJerusalem.txt
WhereToLosAngeles.txt
```

Print the name of the files that contain "romance" in the current directory "berlitz1".

Source:[Link to `grep -l` command](https://www.freecodecamp.org/news/grep-command-in-linux-usage-options-and-syntax-examples/)
