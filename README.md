# Bandit

https://overthewire.org/wargames/bandit/

> The Bandit wargame is aimed at absolute beginners.<br>
> It will teach the basics needed to be able to play other wargames

> You start at Level 0 and try to “beat” or “finish” it. Finishing a level results in information on how to start the next level. The pages on this website for “Level <X>” contain information on how to start level X from the previous level

> Start here:<br>

> bandit.labs.overthewire.org:2220<br>

> Username: bandit0<br>
> Password: bandit0

# Level 0
```console 
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme
```
> Congratulations on your first steps into the bandit game!!<br>
Please make sure you have read the rules at https://overthewire.org/rules/<br>
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

> The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
# Level 1
```console 
ssh bandit1@bandit.labs.overthewire.org -p 2220
ls
cat < -
```
> 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
# Level 2
```console 
ssh bandit2@bandit.labs.overthewire.org -p 2220
ls -l
cat spaces\ in\ this\ filename
```
> MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
# Level 3
```console
ssh bandit3@bandit.labs.overthewire.org -p 2220
ls -l
cd inhere
ls -al
cat ...Hiding-From-You
```
> 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
# Level 4
```console
ssh bandit4@bandit.labs.overthewire.org -p 2220
ls -l
cd inhere
ls -l
cat ./-file07
```
> 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
# Level 5
```console
ssh bandit5@bandit.labs.overthewire.org -p 2220
ls -l
cd inhere
ls -Af
cd maybehere07/
cat .file2
```
> HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
# Level 6
> The password for the next level is stored somewhere on the server and has all of the following properties:

> owned by user bandit7<br>
> owned by group bandit6<br>
> 33 bytes in size<br>
```console
ssh bandit6@bandit.labs.overthewire.org -p 2220
ls -Al
find / -user bandit7 -group bandit6 -size 33c
```
```console
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
[...]
find: ‘/var/lib/amazon’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/lib/apt/lists/partial’: Permission denied
[...]
find: ‘/run/udisks2’: Permission denied
```
```console
cat /var/lib/dpkg/info/bandit7.password
```
> morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
# Level 7
> The password for the next level is stored in the file data.txt next to the word millionth
```console
ssh bandit7@bandit.labs.overthewire.org -p 2220
ls -Al
grep 'millionth' data.txt
```
> millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
# Level 8
> The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
```console
ssh bandit8@bandit.labs.overthewire.org -p 2220
ls -Al
cat data.txt | sort | uniq -u
```
> 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
# Level 9
> The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
```console
ssh bandit9@bandit.labs.overthewire.org -p 2220
ls -Al
strings data.txt | grep ===
```
> }========== the <br>
> 3JprD========== passwordi <br>
> ~fDV3========== is <br>
> D9========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
# Level 10
> The password for the next level is stored in the file data.txt, which contains base64 encoded data
```console
ssh bandit10@bandit.labs.overthewire.org -p 2220
ls -Al
grep -E '[A-Za-z0-9+/]{4}*([A-Za-z0-9+/]{4}|[A-Za-z0-9+/]{3}=|[A-Za-z0-9+/]{2}==)' data.txt
echo VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg== | base64 --decode
```
> The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
# Level 11
> The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
```console
ssh bandit11@bandit.labs.overthewire.org -p 2220
ls -Al
```
> 
