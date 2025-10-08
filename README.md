# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

![WhatsApp Image 2025-10-06 at 17 52 07_fb886e79](https://github.com/user-attachments/assets/7b7bbe30-0b5e-47e8-88bb-e3a84c73cbfb)




cat < file2
## OUTPUT

![WhatsApp Image 2025-10-06 at 17 52 43_604d0cfa](https://github.com/user-attachments/assets/7deff71e-c18c-4318-a750-cf1871783ee0)



# Comparing Files
cmp file1 file2
## OUTPUT

![WhatsApp Image 2025-10-06 at 17 53 30_c6f5171f](https://github.com/user-attachments/assets/53505c53-b896-4a44-9a49-3f759336a7d0)



 
comm file1 file2
 ## OUTPUT

![WhatsApp Image 2025-10-06 at 17 54 11_ddb6ffdf](https://github.com/user-attachments/assets/04f99e11-63c3-4f8c-b9e9-76aebbfb4ccb)




 
diff file1 file2
## OUTPUT

![WhatsApp Image 2025-10-06 at 17 54 35_ec797553](https://github.com/user-attachments/assets/4b673822-38c2-4964-a95a-16c33ea7be35)




#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

![WhatsApp Image 2025-10-06 at 17 56 25_3348e5ee](https://github.com/user-attachments/assets/cbb9af72-658e-4e09-b28e-ff6fb5b1f674)




cut -d "|" -f 1 file22
## OUTPUT

![WhatsApp Image 2025-10-06 at 17 56 42_57db3ff1](https://github.com/user-attachments/assets/5dbf64b7-a43c-42f7-98c5-1ebf2784a14e)



cut -d "|" -f 2 file22
## OUTPUT

![WhatsApp Image 2025-10-06 at 17 57 04_aca285c1](https://github.com/user-attachments/assets/d756d374-6b8d-48fe-a3ef-7cdfd7c4556f)



cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 04 26_a45f24ea](https://github.com/user-attachments/assets/f5c2e5f5-0b72-4d1b-b955-2ab8e5b1cc65)



grep hello newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 04 53_d740ca3d](https://github.com/user-attachments/assets/d4e49b87-f50f-49af-b85a-24cff0cc9943)




grep -v hello newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 05 40_45238042](https://github.com/user-attachments/assets/42058cb9-4198-4b37-9b01-158b4727c8fe)



cat newfile | grep -i "hello"
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 06 04_864a6679](https://github.com/user-attachments/assets/bacfdf78-a290-4b17-9bdb-63d2fb670c89)




cat newfile | grep -i -c "hello"
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 06 37_1c2dc3d7](https://github.com/user-attachments/assets/9e836ac4-6352-4fac-8dc9-eab56e7e6910)




grep -R ubuntu /etc
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 07 35_34d228d4](https://github.com/user-attachments/assets/795224bf-0bc7-4a8c-8966-379f329d8222)



grep -w -n world newfile   
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 08 00_192b1218](https://github.com/user-attachments/assets/f226329d-89b0-4c64-8ae1-52905f984e24)




cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 08 54_baeab182](https://github.com/user-attachments/assets/4a279df5-e8bb-450d-8253-89d675f16941)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 09 25_27757d94](https://github.com/user-attachments/assets/da57fc8d-f0b2-46c3-bb4e-ef293296e46f)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 10 15_d7555906](https://github.com/user-attachments/assets/c1d27149-40c8-4bd6-9bcd-bc7f786a93ca)




egrep '(^hello)' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 12 07_de5afe67](https://github.com/user-attachments/assets/21e1f500-3f83-4339-b8a7-296b24985340)



egrep '(world$)' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 12 28_b93b1807](https://github.com/user-attachments/assets/4aa5ed80-5676-4663-b573-e67b1f78968a)



egrep '(World$)' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 12 54_f4e97669](https://github.com/user-attachments/assets/506536dc-0186-4411-a004-e893c92e3f7a)



egrep '((W|w)orld$)' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 13 27_111b468b](https://github.com/user-attachments/assets/c49d6c1a-2313-4f87-b278-03db9b57ec65)




egrep '[1-9]' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 13 50_527df7ba](https://github.com/user-attachments/assets/742d605c-c029-434a-85ff-5f1ca6efcce0)



egrep 'Linux.*world' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 14 21_ce56bc97](https://github.com/user-attachments/assets/30a4d503-b506-4a06-b3cb-80e890594e2f)



egrep 'Linux.*World' newfile 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 14 57_d5755c14](https://github.com/user-attachments/assets/e5bf46b2-3e47-4f18-82ff-af6703b5c2c3)



egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 15 23_5f9b5eb8](https://github.com/user-attachments/assets/61cab127-747d-460e-95fb-ae6745753a86)



egrep 's{1,2}' newfile
## OUTPUT 

![WhatsApp Image 2025-10-06 at 18 15 45_2f38bca1](https://github.com/user-attachments/assets/460a1ae9-4e27-416f-835c-23155c776ee2)



cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 16 44_7e63efde](https://github.com/user-attachments/assets/a842404a-4f53-4d2f-a2de-10900061afdc)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 17 27_1e292b58](https://github.com/user-attachments/assets/dc6d4a32-b61a-47a1-9f34-7935c7117cc0)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 17 46_430ef07e](https://github.com/user-attachments/assets/e7c6ecf6-3c16-43ef-a6db-9ad944325782)




sed  '/tom/s/5000/6000/' file23
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 18 09_0180fdbf](https://github.com/user-attachments/assets/e51f0838-c95d-441b-979c-fd963b25529d)



sed -n -e '1,5p' file23
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 18 27_44087672](https://github.com/user-attachments/assets/a1020c51-25da-459d-8011-408f19f9165a)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 18 43_76311c56](https://github.com/user-attachments/assets/b6fd0887-2fef-4da6-9f82-ee01e595291c)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 19 06_c9216c7c](https://github.com/user-attachments/assets/8c518c7f-98ea-4c21-af52-ead4e2ec55b0)



seq 10 
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 19 59_1fecb743](https://github.com/user-attachments/assets/09444bf0-6703-46cd-bb8b-8bb80055cab9)



seq 10 | sed -n '4,6p'
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 21 03_9b53a702](https://github.com/user-attachments/assets/62babfee-002c-410a-b113-0cd203862b2b)



seq 10 | sed -n '2,~4p'
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 21 16_84c5ee9b](https://github.com/user-attachments/assets/ca63f0a6-0607-4aa0-a22d-8d6474cf7a60)



seq 3 | sed '2a hello'
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 21 48_bb640ab7](https://github.com/user-attachments/assets/50675f34-d547-4464-8222-a7450170f01e)



seq 2 | sed '2i hello'
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 22 13_5462843f](https://github.com/user-attachments/assets/2afd2b05-3f48-4fe2-9406-17994e19ccd2)



seq 10 | sed '2,9c hello'
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 22 42_177f205b](https://github.com/user-attachments/assets/2e755939-ba92-4909-b36f-ef371ef2e54a)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 23 09_1d79e043](https://github.com/user-attachments/assets/7eb77e97-53fa-4523-bda3-942c76fedbb1)



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 24 24_8fab3df8](https://github.com/user-attachments/assets/a7efaa42-d7ec-4185-a499-798ce5d3cfe1)



cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 25 01_8807f8b9](https://github.com/user-attachments/assets/60efe219-8bbc-437c-8a3f-8308ba39d6cf)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![WhatsApp Image 2025-10-06 at 18 25 24_06eea011](https://github.com/user-attachments/assets/c487e906-d7e0-4227-8316-00267bd8ac17)




cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

![WhatsApp Image 2025-10-06 at 18 26 36_c248a3b5](https://github.com/user-attachments/assets/fd1bc870-24db-4bfa-bdd5-ed0b417bf683)




#Backup commands
tar -cvf backup.tar *
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 27 25_12a59141](https://github.com/user-attachments/assets/4cd6ba62-41a4-4ee5-8758-2edda02b021c)



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 28 45_e4d13a26](https://github.com/user-attachments/assets/de539ef3-e689-4d83-8c84-3f388ba63abc)




tar -xvf backup.tar
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 28 59_c09ade43](https://github.com/user-attachments/assets/bcd51111-0854-4b02-8b48-b8c255539e44)




gzip backup.tar

ls .gz
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 31 41_a1b19cb7](https://github.com/user-attachments/assets/dca776f7-89e8-4b69-9325-a760efa6b991)


 
gunzip backup.tar.gz
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 32 39_96f724d5](https://github.com/user-attachments/assets/d337bc09-81cd-4ffd-a7e7-7be06f0adfb7)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```


cat herecheck.txt
## OUTPUT
![WhatsApp Image 2025-10-06 at 18 36 17_39cf3b44](https://github.com/user-attachments/assets/5b2d422d-a0c0-44ba-8494-124847610e3e)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![WhatsApp Image 2025-10-06 at 18 38 24_187533fe](https://github.com/user-attachments/assets/73b46e6b-02b8-454a-b2a2-5d9114955b5e)

 
ls file1
## OUTPUT
![WhatsApp Image 2025-10-06 at 18 38 41_4044aea8](https://github.com/user-attachments/assets/8ca875a0-3eb2-41aa-be9b-809f75f7d6ea)

echo $?
## OUTPUT 
![WhatsApp Image 2025-10-06 at 18 41 01_90e9c5f7](https://github.com/user-attachments/assets/eb1c9543-3c6b-44be-93ba-04eb7d81747c)




 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![WhatsApp Image 2025-10-06 at 18 42 49_d65539b0](https://github.com/user-attachments/assets/122ed363-ea90-4c33-870c-de31d03032c3)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

![WhatsApp Image 2025-10-06 at 18 43 32_728b4a14](https://github.com/user-attachments/assets/c3a74f52-9a55-4574-ac3c-38a2dd62990f)


# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
![WhatsApp Image 2025-10-06 at 18 50 05_f71e0577](https://github.com/user-attachments/assets/5a168144-ae15-4ac9-a2dd-50fc181af0a4)



# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![WhatsApp Image 2025-10-06 at 18 51 45_d0f59d42](https://github.com/user-attachments/assets/7aeb5758-26a7-4b2a-b59e-43038865aa6d)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![WhatsApp Image 2025-10-06 at 18 53 53_73cef2a2](https://github.com/user-attachments/assets/558711ac-cbb9-49f1-a074-21305229b680)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 

## OUTPUT
![WhatsApp Image 2025-10-06 at 18 54 39_c083e547](https://github.com/user-attachments/assets/4b59c7bd-8bc7-4f66-8a22-418ee88f59a3)

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## OUTPUT
![WhatsApp Image 2025-10-06 at 18 56 30_c2b1f0c2](https://github.com/user-attachments/assets/5774a2c9-3705-4d01-98eb-55775d3bf9a9)

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 ## OUTPUT
 
 ![WhatsApp Image 2025-10-06 at 18 57 37_969a55a8](https://github.com/user-attachments/assets/8ae94cc0-a84f-4b32-98d6-f32fd0ce1790)

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
## OUTOUT
![WhatsApp Image 2025-10-06 at 19 01 25_4649dcdb](https://github.com/user-attachments/assets/bf83044d-dc5d-45df-a6bc-382e4d6c3307)


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 ![WhatsApp Image 2025-10-06 at 19 07 33_5e27d9ef](https://github.com/user-attachments/assets/bc3128aa-9cd8-48cf-98ae-71e5b9977b7b)






# RESULT:
The Commands are executed successfully.
