
# Lab Report 3 - Researching Commands

## ``grep -c`` Command Line Option

The ``grep -c`` command line option searches through the file and prints the total amount of times the specific string appears in the file. It is not case sensitive and is really useful if you want to count the total amount of times a keyword is said in a book.

### ``grep -c`` Example #1

```BASH
Leo Cruz@DESKTOP-B9LT90S MINGW64 ~/Documents/My_Git_Repository/docsearch (main)
$ grep -c "The" written_2/non-fiction/OUP/Abernathy/*.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt:50
written_2/non-fiction/OUP/Abernathy/ch14.txt:35
written_2/non-fiction/OUP/Abernathy/ch15.txt:50
written_2/non-fiction/OUP/Abernathy/ch2.txt:46
written_2/non-fiction/OUP/Abernathy/ch3.txt:33
written_2/non-fiction/OUP/Abernathy/ch6.txt:34
written_2/non-fiction/OUP/Abernathy/ch7.txt:39
written_2/non-fiction/OUP/Abernathy/ch8.txt:47
written_2/non-fiction/OUP/Abernathy/ch9.txt:33
```

In this example I am searching through texts of the subdirectory Abernathy and using -c to specify that I am looking for instances of the word "The". Since this option is not case sensitive as you can see through the example the word "the" for the first text file appears 50 times, whether that be "THE" "the" "The" or "tHe".

### ``grep -c`` Example #2

```BASH
Leo Cruz@DESKTOP-B9LT90S MINGW64 ~/Documents/My_Git_Repository/docsearch (main)
$ grep -c "and" written_2/non-fiction/OUP/Berk/*.txt
written_2/non-fiction/OUP/Berk/ch1.txt:143
written_2/non-fiction/OUP/Berk/ch2.txt:158
written_2/non-fiction/OUP/Berk/CH4.txt:170
written_2/non-fiction/OUP/Berk/ch7.txt:124
```

In this example I am searching through the texts of the subdirectory Berk and using -c to count how many times the string "and" appears on each text. The resulting output shows that "and" appears a lot in all of these texts. The output gives us the working path to the text and the amount of times "and" appears in the form of a number.

## ``grep -r`` Command Line Option

The ``grep -r`` command line argument allows you to recursively search through the directory and subdirectories. This is really useful in combination with the ``-c`` command line option to recursively go through a directory instead of manually inputting each subdirectory. I also use the ``-c`` command line due to the output of ``-r`` also printing out the line that the string appears in.

### ``grep -r`` Example #1

```BASH
Leo Cruz@DESKTOP-B9LT90S MINGW64 ~/Documents/My_Git_Repository/docsearch (main)
$ grep -r -c "the" written_2/travel_guides/
written_2/travel_guides/berlitz1/HandRHawaii.txt:64
written_2/travel_guides/berlitz1/HandRHongKong.txt:6
written_2/travel_guides/berlitz1/HandRIbiza.txt:4
written_2/travel_guides/berlitz1/HandRIsrael.txt:113
written_2/travel_guides/berlitz1/HandRIstanbul.txt:4
written_2/travel_guides/berlitz1/HandRJamaica.txt:66
written_2/travel_guides/berlitz1/HandRJerusalem.txt:5
written_2/travel_guides/berlitz1/HandRLakeDistrict.txt:9
written_2/travel_guides/berlitz1/HandRLasVegas.txt:8
written_2/travel_guides/berlitz1/HandRLisbon.txt:5
written_2/travel_guides/berlitz1/HandRLosAngeles.txt:2
written_2/travel_guides/berlitz1/HandRMadeira.txt:10
written_2/travel_guides/berlitz1/HandRMadrid.txt:72
written_2/travel_guides/berlitz1/HandRMallorca.txt:9
written_2/travel_guides/berlitz1/HistoryDublin.txt:141
written_2/travel_guides/berlitz1/HistoryEdinburgh.txt:197
written_2/travel_guides/berlitz1/HistoryEgypt.txt:153
written_2/travel_guides/berlitz1/HistoryFrance.txt:349
written_2/travel_guides/berlitz1/HistoryFWI.txt:133
written_2/travel_guides/berlitz1/HistoryGreek.txt:191
written_2/travel_guides/berlitz1/HistoryHawaii.txt:142
written_2/travel_guides/berlitz1/HistoryHongKong.txt:126
written_2/travel_guides/berlitz1/HistoryIbiza.txt:126
written_2/travel_guides/berlitz1/HistoryIndia.txt:503
written_2/travel_guides/berlitz1/HistoryIsrael.txt:175
written_2/travel_guides/berlitz1/HistoryIstanbul.txt:260
written_2/travel_guides/berlitz1/HistoryItaly.txt:420
written_2/travel_guides/berlitz1/HistoryJamaica.txt:166
written_2/travel_guides/berlitz1/HistoryJapan.txt:374
written_2/travel_guides/berlitz1/HistoryJerusalem.txt:174
written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt:134
written_2/travel_guides/berlitz1/HistoryLasVegas.txt:171
written_2/travel_guides/berlitz1/HistoryMadeira.txt:104
written_2/travel_guides/berlitz1/HistoryMadrid.txt:111
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:332
written_2/travel_guides/berlitz1/HistoryMallorca.txt:127
written_2/travel_guides/berlitz1/IntroDublin.txt:71
written_2/travel_guides/berlitz1/IntroEdinburgh.txt:84
written_2/travel_guides/berlitz1/IntroEgypt.txt:75
written_2/travel_guides/berlitz1/IntroFrance.txt:102
written_2/travel_guides/berlitz1/IntroFWI.txt:63
written_2/travel_guides/berlitz1/IntroGreek.txt:87
written_2/travel_guides/berlitz1/IntroHongKong.txt:44
written_2/travel_guides/berlitz1/IntroIbiza.txt:59
written_2/travel_guides/berlitz1/IntroIndia.txt:216
written_2/travel_guides/berlitz1/IntroIsrael.txt:43
written_2/travel_guides/berlitz1/IntroIstanbul.txt:72
written_2/travel_guides/berlitz1/IntroItaly.txt:116
written_2/travel_guides/berlitz1/IntroJamaica.txt:85
written_2/travel_guides/berlitz1/IntroJapan.txt:156
written_2/travel_guides/berlitz1/IntroJerusalem.txt:86
written_2/travel_guides/berlitz1/IntroLakeDistrict.txt:108
written_2/travel_guides/berlitz1/IntroLasVegas.txt:98
written_2/travel_guides/berlitz1/IntroLosAngeles.txt:48
written_2/travel_guides/berlitz1/IntroMadeira.txt:74
written_2/travel_guides/berlitz1/IntroMadrid.txt:86
written_2/travel_guides/berlitz1/IntroMalaysia.txt:74
written_2/travel_guides/berlitz1/IntroMallorca.txt:74
written_2/travel_guides/berlitz1/JungleMalaysia.txt:61
written_2/travel_guides/berlitz1/WhatToDublin.txt:134
written_2/travel_guides/berlitz1/WhatToEdinburgh.txt:172
written_2/travel_guides/berlitz1/WhatToEgypt.txt:161
written_2/travel_guides/berlitz1/WhatToFrance.txt:11
written_2/travel_guides/berlitz1/WhatToFWI.txt:181
written_2/travel_guides/berlitz1/WhatToGreek.txt:159
written_2/travel_guides/berlitz1/WhatToHawaii.txt:26
written_2/travel_guides/berlitz1/WhatToHongKong.txt:162
written_2/travel_guides/berlitz1/WhatToIbiza.txt:264
written_2/travel_guides/berlitz1/WhatToIndia.txt:157
written_2/travel_guides/berlitz1/WhatToIsrael.txt:159
written_2/travel_guides/berlitz1/WhatToIstanbul.txt:160
written_2/travel_guides/berlitz1/WhatToItaly.txt:167
written_2/travel_guides/berlitz1/WhatToJamaica.txt:784
written_2/travel_guides/berlitz1/WhatToJapan.txt:274
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:180
written_2/travel_guides/berlitz1/WhatToLasVegas.txt:350
written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:167
written_2/travel_guides/berlitz1/WhatToMadeira.txt:202
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:167
written_2/travel_guides/berlitz1/WhatToMallorca.txt:119
written_2/travel_guides/berlitz1/WhereToDublin.txt:723
written_2/travel_guides/berlitz1/WhereToEdinburgh.txt:762
written_2/travel_guides/berlitz1/WhereToEgypt.txt:844
written_2/travel_guides/berlitz1/WhereToFrance.txt:2348
written_2/travel_guides/berlitz1/WhereToFWI.txt:525
written_2/travel_guides/berlitz1/WhereToGreek.txt:795
written_2/travel_guides/berlitz1/WhereToHawaii.txt:18
written_2/travel_guides/berlitz1/WhereToHongKong.txt:548
written_2/travel_guides/berlitz1/WhereToIbiza.txt:379
written_2/travel_guides/berlitz1/WhereToIndia.txt:1698
written_2/travel_guides/berlitz1/WhereToIsrael.txt:786
written_2/travel_guides/berlitz1/WhereToIstanbul.txt:873
written_2/travel_guides/berlitz1/WhereToItaly.txt:2684
written_2/travel_guides/berlitz1/WhereToJapan.txt:1647
written_2/travel_guides/berlitz1/WhereToJerusalem.txt:790
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt:828
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:645
written_2/travel_guides/berlitz1/WhereToMadeira.txt:558
written_2/travel_guides/berlitz1/WhereToMadrid.txt:665
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:1634
written_2/travel_guides/berlitz1/WhereToMallorca.txt:655
written_2/travel_guides/berlitz2/Algarve-History.txt:32
written_2/travel_guides/berlitz2/Algarve-Intro.txt:21
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt:43
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:147
written_2/travel_guides/berlitz2/Amsterdam-History.txt:37
written_2/travel_guides/berlitz2/Amsterdam-Intro.txt:13
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt:43
written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt:120
written_2/travel_guides/berlitz2/Athens-History.txt:44
written_2/travel_guides/berlitz2/Athens-Intro.txt:15
written_2/travel_guides/berlitz2/Athens-WhatToDo.txt:45
written_2/travel_guides/berlitz2/Athens-WhereToGo.txt:126
written_2/travel_guides/berlitz2/Bahamas-History.txt:30
written_2/travel_guides/berlitz2/Bahamas-Intro.txt:17
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt:45
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt:130
written_2/travel_guides/berlitz2/Bali-History.txt:25
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt:42
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt:165
written_2/travel_guides/berlitz2/Barcelona-History.txt:22
written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt:33
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt:124
written_2/travel_guides/berlitz2/Beijing-History.txt:24
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt:45
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt:113
written_2/travel_guides/berlitz2/Berlin-History.txt:45
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt:40
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt:168
written_2/travel_guides/berlitz2/Bermuda-history.txt:29
written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt:62
written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt:97
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:149
written_2/travel_guides/berlitz2/Budapest-History.txt:34
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt:49
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt:155
written_2/travel_guides/berlitz2/California-History.txt:40
written_2/travel_guides/berlitz2/California-WhatToDo.txt:49
written_2/travel_guides/berlitz2/California-WhereToGo.txt:151
written_2/travel_guides/berlitz2/Canada-History.txt:71
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:423
written_2/travel_guides/berlitz2/CanaryIslands-History.txt:28
written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt:50
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:117
written_2/travel_guides/berlitz2/Cancun-History.txt:21
written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt:44
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt:110
written_2/travel_guides/berlitz2/China-History.txt:63
written_2/travel_guides/berlitz2/China-WhatToDo.txt:42
written_2/travel_guides/berlitz2/China-WhereToGo.txt:415
written_2/travel_guides/berlitz2/Costa-History.txt:33
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt:42
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt:137
written_2/travel_guides/berlitz2/CostaBlanca-History.txt:27
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:75
written_2/travel_guides/berlitz2/Crete-History.txt:33
written_2/travel_guides/berlitz2/Crete-WhatToDo.txt:50
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt:135
written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt:115
written_2/travel_guides/berlitz2/Cuba-History.txt:27
written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt:31
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt:149
written_2/travel_guides/berlitz2/Nepal-History.txt:36
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt:81
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt:104
written_2/travel_guides/berlitz2/NewOrleans-History.txt:43
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt:31
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:146
written_2/travel_guides/berlitz2/Poland-History.txt:37
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt:36
written_2/travel_guides/berlitz2/Portugal-History.txt:39
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt:48
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt:281
written_2/travel_guides/berlitz2/PuertoRico-History.txt:22
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt:57
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:116
written_2/travel_guides/berlitz2/Vallarta-History.txt:32
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt:61
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:111
```

In this example I have a directory called travel_guides that contains two subdirectories berlitz1 and berlitz2. Instead of manually running each command for each sub directory I use the ``grep -r`` command to recursively search for the string "the" through both the subdirectories. The reason I used the ``-c`` command is because when using the ``-r`` command it prints out the line the string appears on and it would clutter up the terminal too much.

### ``grep -r`` Example #2

```BASH
Leo Cruz@DESKTOP-B9LT90S MINGW64 ~/Documents/My_Git_Repository/docsearch (main)
$ grep -r -c "among themselves" written_2/non-fiction/
written_2/non-fiction/OUP/Abernathy/ch1.txt:0
written_2/non-fiction/OUP/Abernathy/ch14.txt:0
written_2/non-fiction/OUP/Abernathy/ch15.txt:0
written_2/non-fiction/OUP/Abernathy/ch2.txt:0
written_2/non-fiction/OUP/Abernathy/ch3.txt:0
written_2/non-fiction/OUP/Abernathy/ch6.txt:0
written_2/non-fiction/OUP/Abernathy/ch7.txt:0
written_2/non-fiction/OUP/Abernathy/ch8.txt:0
written_2/non-fiction/OUP/Abernathy/ch9.txt:0
written_2/non-fiction/OUP/Berk/ch1.txt:0
written_2/non-fiction/OUP/Berk/ch2.txt:0
written_2/non-fiction/OUP/Berk/CH4.txt:0
written_2/non-fiction/OUP/Berk/ch7.txt:0
written_2/non-fiction/OUP/Castro/chA.txt:0
written_2/non-fiction/OUP/Castro/chB.txt:1
written_2/non-fiction/OUP/Castro/chC.txt:0
written_2/non-fiction/OUP/Castro/chL.txt:0
written_2/non-fiction/OUP/Castro/chM.txt:0
written_2/non-fiction/OUP/Castro/chN.txt:0
written_2/non-fiction/OUP/Castro/chO.txt:0
written_2/non-fiction/OUP/Castro/chP.txt:0
written_2/non-fiction/OUP/Castro/chQ.txt:0
written_2/non-fiction/OUP/Castro/chR.txt:0
written_2/non-fiction/OUP/Castro/chV.txt:0
written_2/non-fiction/OUP/Castro/chW.txt:0
written_2/non-fiction/OUP/Castro/chY.txt:0
written_2/non-fiction/OUP/Castro/chZ.txt:0
written_2/non-fiction/OUP/Fletcher/ch1.txt:0
written_2/non-fiction/OUP/Fletcher/ch10.txt:0
written_2/non-fiction/OUP/Fletcher/ch2.txt:1
written_2/non-fiction/OUP/Fletcher/ch5.txt:0
written_2/non-fiction/OUP/Fletcher/ch6.txt:0
written_2/non-fiction/OUP/Fletcher/ch9.txt:0
written_2/non-fiction/OUP/Kauffman/ch1.txt:0
written_2/non-fiction/OUP/Kauffman/ch10.txt:0
written_2/non-fiction/OUP/Kauffman/ch3.txt:0
written_2/non-fiction/OUP/Kauffman/ch4.txt:0
written_2/non-fiction/OUP/Kauffman/ch5.txt:0
written_2/non-fiction/OUP/Kauffman/ch6.txt:0
written_2/non-fiction/OUP/Kauffman/ch7.txt:0
written_2/non-fiction/OUP/Kauffman/ch8.txt:0
written_2/non-fiction/OUP/Kauffman/ch9.txt:0
written_2/non-fiction/OUP/Rybczynski/ch1.txt:0
written_2/non-fiction/OUP/Rybczynski/ch2.txt:0
written_2/non-fiction/OUP/Rybczynski/ch3.txt:0
```

In this example I am looking through the subdirectory OUP in the non-fiction directory. In this subdirectory there are many subdirectories named after the authors of each text. It would be a labor to manually type each ``grep "this"`` for each sub directory so I recursively go through each text file and look if there is an instance of "among themselves" in the text.

## ``grep -i`` Command Line Argument

The ``grep -i`` command line argument performs a case sensitive search for the keyword you input. This is useful incase you want to differentiate between different words that might contain accents.

### ``grep -i`` Example #1

```BASH
Leo Cruz@DESKTOP-B9LT90S MINGW64 ~/Documents/My_Git_Repository/docsearch (main)
$ grep -i "Limón" written_2/non-fiction/OUP/Castro/chB.txt
Robe’s collection of New Mexico legends contains thirty-four variants of the devil-at-the-dance tale. Although the legends in this collection are from rural northern New Mexico, collected in the 1950s and 1960s, we find contemporary versions of the devil-at-the-dance tales in south Texas and in Baja California from the 1980s. Limón 
and Herrera-Sobek discuss versions of the tale circulating in nightclubs and discotheques among urbanized young people.
References De Leon 1982; Glazer 1984,1994; Herrera-Sobek 1988; Limón 1994; Martin 1983; Robe 1951; Robe ed. 1980; West 1988
Most Mexican national holiday celebrations such as Cinco de Mayo and El Diez y Seis de Septiembre will end with a community dance. Even in modern times, professional Latino and Chicano associations often close their national conferences with a baile, bringing in popular Chicano bands. Jose Limón discusses the narratives of bailando 
con el diablo (dancing with the devil), and Manuel Peña shows us the ritualized structure of a Chicano dance.
References Bell 1927; De Leon 1982; Limón 1983, 1994; Peña 1980, 1985b; Shay 1982
References Limón 1994; New Handbook of Texas 1996
```

In this example I use the command ``grep -i`` to search for the string "Limón" which contains an accent on the o. using ``-i`` makes the search case sensitive so the output on my terminal gives the the line where "Limón" appears but not where "Limon" appears on the text.

### ``grep -i`` Example #2 

```BASH
Leo Cruz@DESKTOP-B9LT90S MINGW64 ~/Documents/My_Git_Repository/docsearch (main)
$ grep -i "Coconstructing" written_2/non-fiction/OUP/Kauffman/ch10.txt 
A Coconstructing Cosmos?
Coconstructing Complexity?
```

## ``grep -n`` Command Line Argument

The ``grep -n`` command line argument displays the matched lines and what line number they appear on. This is helpful if you want to search a tourist attraction and learn more about it.]

### ``grep -n`` Example #1

```BASH
Leo Cruz@DESKTOP-B9LT90S MINGW64 ~/Documents/My_Git_Repository/docsearch (main)
$ grep -n "relaxing" written_2/travel_guides/berlitz1/*.txt
written_2/travel_guides/berlitz1/HandRHawaii.txt:152:        floors, private gardens, and spacious lanais create a relaxing hideaway
written_2/travel_guides/berlitz1/HandRIsrael.txt:290:        Young, friendly, Christian staff, quiet relaxing atmosphere to soothe  
written_2/travel_guides/berlitz1/IntroLakeDistrict.txt:28:        combined, create the most pleasing and relaxing vistas
written_2/travel_guides/berlitz1/WhatToEgypt.txt:295:        you can have a relaxing swim and some “kid” fun. For children too young
written_2/travel_guides/berlitz1/WhatToGreek.txt:7:        Island life is certainly relaxing, and in the Aegean there
written_2/travel_guides/berlitz1/WhatToIbiza.txt:524:        off-limits — it’s just too relaxing.
written_2/travel_guides/berlitz1/WhatToJamaica.txt:99:        morning or full day out at sea for sport fishing or just a relaxing
written_2/travel_guides/berlitz1/WhatToJamaica.txt:218:        cool and relaxing way to be pushed along, almost like a tropical
written_2/travel_guides/berlitz1/WhatToJamaica.txt:1094:        the dark, volcanic sand. You’ll be able to spend the day relaxing
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:19:        are particularly relaxing: They often take in areas of forest, such as
written_2/travel_guides/berlitz1/WhereToEgypt.txt:1092:        beaches it offers all the basic ingredients needed for a relaxing
written_2/travel_guides/berlitz1/WhereToFrance.txt:34:        relaxing vacation, for example, might combine Paris and the
written_2/travel_guides/berlitz1/WhereToFrance.txt:933:        mounds, and shady woods, are English in style — a relaxing change from
written_2/travel_guides/berlitz1/WhereToFrance.txt:1022:        its park and you can also enjoy a relaxing view from a tethered hot-air
written_2/travel_guides/berlitz1/WhereToFrance.txt:3235:        pleasant countryside and towns and the joy of driving on more relaxing
written_2/travel_guides/berlitz1/WhereToHongKong.txt:168:        The World of Suzy Wong. Servicemen relaxing from the rigors of the
written_2/travel_guides/berlitz1/WhereToIbiza.txt:30:        tempted to stay put for a while, relaxing in one of the Mediterranean’s
written_2/travel_guides/berlitz1/WhereToIndia.txt:660:        Kashmir at the end, with the intention of relaxing in a houseboat on a
written_2/travel_guides/berlitz1/WhereToIndia.txt:1117:        relaxing in the side niches at the entrance. Visit Cave 26 for a riot
written_2/travel_guides/berlitz1/WhereToIsrael.txt:513:        perfect size for relaxing away a couple of hours on a wet day.
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt:866:        Water ferry moors. The lake ferry provides a relaxing way to take in
written_2/travel_guides/berlitz1/WhereToMadeira.txt:645:        Ribeiro Frio is relaxing, but the real reason for its
```

In this example I use ``grep -n "relaxing"`` to search what line the string appears on each text of the berlitz1 subdirectory and the line that it appears on. This is somewhat like the combination of ``grep -c`` and the normal command of grep. As shown on the terminal code block we see the number of the line the string appears on and the actual line the string appears on.

```BASH
Leo Cruz@DESKTOP-B9LT90S MINGW64 ~/Documents/My_Git_Repository/docsearch (main)
$ grep -n "delicious" written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt
36:From the center of town, head to the waterfront, especially if it’s anywhere near time for lunch or dinner. You can almost follow your nose toward the heady aroma of grilled sardines. It will take you to the dockside, lined with simple restaurants, one after the other, all serving delicious, smoky sardines (and other fresh-caught fish). Choose whichever spot seems to be bustling with ravenous patrons. A plate of grilled sardines, prawns, or squid and a bottle of house wine make a fantastic meal, and the prices are about as low as anywhere along the coast.
```

In this example I use ``grep -n "delicious"`` in the text file Algarve-WhereToGo.txt. Just like before it gives me the line number where the String resides at and the actual line where the string appears on.
