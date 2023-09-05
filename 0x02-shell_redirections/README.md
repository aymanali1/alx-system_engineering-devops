0x02. Shell, I/O Redirections and filters

alx-system_engineering-devops
0x02-shell_redirections

0. Hello World
0-hello_world
#!/bin/bash
echo “Hello, world”

1. Confused smiley
1-confused_smiley
#!/bin/bash
echo “\"(Ôo)'”

2. Let's display a file
2-hellofile
#!/bin/bash
cat /etc/passwd

3. What about 2?
3-twofiles
#!/bin/bash
cat /etc/passwd /etc/hosts

4. Last lines of a file
4-lastlines
#!/bin/bash
tail -n 10 /etc/passwd
5. I'd prefer the first ones actually
5-firstlines
#!/bin/bash
head -n 10 /etc/passwd

6. Line #2
6-third_line
#!/bin/bash
head -n 3 iacta | tail -n 1
 
7. It is a good file that cuts iron without making a noise
7-file
#!/bin/bash
echo “Best School” > \*\\'"Best School"\'\\*$\?\*\*\*\*\*:)

8. Save current state of directory
8-cwd_state
#!/bin/bash
echo “ls-la” > ls_cwd_content


9. Duplicate last line
9-duplicate_last_line
#!/bin/bash
tail -n 1 iacta >> iacta 

10. No more javascript
10-no_more_js
#!/bin/bash
find . -type f -name “*.js” -delete



11. Don't just count your directories, make your directories count
11-directories
#!/bin/bash
find . -type d -not -name | wc -l

12. What’s new
12-newest_files
#!/bin/bash
ls -tl | head -n 10


13. Being unique is better than being perfect
13-unique
#!/bin/bash
sort | uniq -u 


14. It must be in that file
14-findthatword
#!/bin/bash
grep -i “root” /etc/passwd



15. Count that word
15-countthatword
#!/bin/bash
grep -c -i “bin” /etc/passwd



16. What's next?
16-whatsnext
#!/bin/bash
grep -i “root” -A 3 /etc/passwd

17. I hate bins
17-hidethisword
#!/bin/bash
grep -i -v "bin" /etc/passwd



18. Letters only please
18-letteronly
#!/bin/bash
grep -i "^[a-z]" /etc/ssh/sshd_config


19. A to Z
19-AZ
#!/bin/bash
tr "A" "Z" | tr "c" "e"



20. Without C, you would live in hiago
20-hiago
#!/bin/bash
tr -d “cC”


21. esreveR
21-reverse
#!/bin/bash
rev

22. DJ Cut Killer
22-users_and_homes
#!/bin/bash
cut -d ':' -f 1,6 /etc/passwd | sort


23. Empty casks make the most noise
100-empty_casks
#!/bin/bash
find . -empty | rev | cut -d '/' -f 1 | rev

24. A gif is worth ten thousand words
101-gifs
#!/bin/bash
find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d '.' -f 2- | rev | LC_ALL=C sort -f


25. Acrostic
102-acrostic
#!/bin/bash
cut -c 1 | paste -s -d ''

26. The biggest fan
103-the_biggest_fan
#!/bin/bash
tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev

