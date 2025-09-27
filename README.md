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

<img width="361" height="176" alt="image" src="https://github.com/user-attachments/assets/0157b375-478a-458c-9e54-c0008a70034d" />



cat < file2
## OUTPUT

<img width="420" height="76" alt="image" src="https://github.com/user-attachments/assets/d04143dd-4534-4dbf-b81a-fad99b667b2a" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="453" height="303" alt="image" src="https://github.com/user-attachments/assets/7c3ef1b8-74ad-49c6-b0df-c086059ad9a8" />


 
comm file1 file2
 ## OUTPUT

<img width="527" height="275" alt="image" src="https://github.com/user-attachments/assets/8b4e79aa-baa0-4b67-8ac0-9cb4c1d78871" />



 
diff file1 file2
## OUTPUT

![Uploading image.png…]()


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

<img width="692" height="65" alt="cut1" src="https://github.com/user-attachments/assets/35251099-cde4-42d9-9b00-9e2f5a1832d1" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="691" height="78" alt="cut2" src="https://github.com/user-attachments/assets/bb0d0424-c301-4588-b23a-c77001aa47dd" />


cut -d "|" -f 2 file22
## OUTPUT


<img width="688" height="79" alt="cut3" src="https://github.com/user-attachments/assets/0ebea1cc-2d80-40a3-aae6-a1ecb85cd7fe" />


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

<img width="692" height="44" alt="grep1" src="https://github.com/user-attachments/assets/393e5dab-8702-4c94-b7c3-60ec2757ce7d" />


grep hello newfile 
## OUTPUT

<img width="692" height="44" alt="grep2" src="https://github.com/user-attachments/assets/5d898378-423c-4bfc-a3a8-5146dab66edc" />



grep -v hello newfile 
## OUTPUT

<img width="692" height="44" alt="grep3" src="https://github.com/user-attachments/assets/a232bdf7-e805-48ab-88ca-e410a0d8737c" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="716" height="60" alt="grep4" src="https://github.com/user-attachments/assets/bbe400ef-a30b-43eb-bf84-acb1270209b9" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="751" height="43" alt="grep5" src="https://github.com/user-attachments/assets/9966d2da-a636-46d4-96e6-172c65afca40" />



grep -R ubuntu /etc
## OUTPUT

<img width="1285" height="414" alt="grep6" src="https://github.com/user-attachments/assets/c8a4b718-fc8a-4375-9f42-f1e3e67ec24f" />


grep -w -n world newfile   
## OUTPUT

<img width="819" height="62" alt="grep7" src="https://github.com/user-attachments/assets/cd42dbc1-a986-4087-9b4e-e95eda53b57d" />



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

<img width="819" height="62" alt="egrep" src="https://github.com/user-attachments/assets/d319da95-f16f-4dcd-96f9-6cea68bcb80a" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="819" height="62" alt="egrep1" src="https://github.com/user-attachments/assets/d24d93f7-867c-409a-ad66-b96135d8c103" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="819" height="62" alt="egrep2" src="https://github.com/user-attachments/assets/c775398b-1a58-437d-88f1-7c45535069cb" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="817" height="44" alt="egrep3" src="https://github.com/user-attachments/assets/c0269fd7-cbc1-435e-aaba-05ba63b4171a" />


egrep '(world$)' newfile 
## OUTPUT

<img width="820" height="57" alt="egrep4" src="https://github.com/user-attachments/assets/cbe47c80-6016-4b2c-9970-15170e73a51f" />


egrep '(World$)' newfile 
## OUTPUT

<img width="820" height="42" alt="egrep5" src="https://github.com/user-attachments/assets/20ce3418-81d8-4f3e-b3e3-4a3fd9d91304" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="822" height="78" alt="egrep6" src="https://github.com/user-attachments/assets/5a2fe7f2-aa83-434d-a6a8-eafb31f133ad" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="819" height="41" alt="egrep7" src="https://github.com/user-attachments/assets/870fd78a-2dba-4271-ba3e-ffa2246f2ac6" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="819" height="41" alt="egrep8" src="https://github.com/user-attachments/assets/2f56906e-dd33-46a6-a29a-ad2c08dd6b96" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="819" height="41" alt="egrep9" src="https://github.com/user-attachments/assets/48f56eb1-23ab-4a58-a8a1-49c3b44ac6e4" />


egrep l{2} newfile
## OUTPUT

<img width="821" height="62" alt="egrep10" src="https://github.com/user-attachments/assets/d3b03a02-80a9-4e8e-8b99-9fff05ae242d" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="822" height="78" alt="egrep11" src="https://github.com/user-attachments/assets/d49e5e86-35d1-4e43-bea4-fcc0a0096dfa" />


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

<img width="707" height="44" alt="sed" src="https://github.com/user-attachments/assets/bfe3c2f9-c82f-4248-ad76-95a08ac254f9" />


sed -n -e '$p' file23
## OUTPUT

<img width="707" height="44" alt="sed1" src="https://github.com/user-attachments/assets/6e2492d8-d76e-4ed9-9f07-981de456b4ff" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="718" height="166" alt="sed2" src="https://github.com/user-attachments/assets/d4d28448-3618-4dd5-aa3d-adc6a05dfb1d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="718" height="166" alt="sed3" src="https://github.com/user-attachments/assets/0ed791b6-8ed9-44ab-b8a6-afc3372cacb5" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="718" height="166" alt="sed4" src="https://github.com/user-attachments/assets/677ec2e7-ea92-474c-8735-0d33d6801afb" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="718" height="111" alt="sed5" src="https://github.com/user-attachments/assets/f73c1e6c-4472-4bdc-b28e-94ec473f09ed" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="718" height="78" alt="sed6" src="https://github.com/user-attachments/assets/94c2b6a2-40bc-4360-a6c2-383b75a120e3" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="738" height="59" alt="sed7" src="https://github.com/user-attachments/assets/9207c9d4-9b84-4102-a8f5-c92c46b7c2c9" />


seq 10 
## OUTPUT

<img width="738" height="202" alt="seq" src="https://github.com/user-attachments/assets/1a862ebd-ad18-421f-a157-574c3d030bbc" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="738" height="81" alt="seq1" src="https://github.com/user-attachments/assets/20f7b2fa-bba1-40c3-ba8a-02e6b685107e" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="738" height="81" alt="seq2" src="https://github.com/user-attachments/assets/188db4ea-eda8-4b5a-889e-c7a68bc12ce1" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="738" height="93" alt="seq3" src="https://github.com/user-attachments/assets/4445a5dd-efb0-455c-80fe-21acc7171cdd" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="738" height="86" alt="seq4" src="https://github.com/user-attachments/assets/ea23a766-b031-4c5a-9afd-be5cc83d885f" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="738" height="83" alt="seq5" src="https://github.com/user-attachments/assets/7df52347-8c5b-4c46-a1c4-7329aaaefafc" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="738" height="83" alt="sed-n" src="https://github.com/user-attachments/assets/1efaf0e2-de32-4914-9658-7e0ecc124f6a" />


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

<img width="738" height="115" alt="sort" src="https://github.com/user-attachments/assets/6b03e9e4-200b-42ab-87dd-36fab3a3718a" />


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

<img width="738" height="115" alt="uniq" src="https://github.com/user-attachments/assets/4a2e0985-750d-4d4e-ae8b-5fabfe76aba8" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="782" height="169" alt="1" src="https://github.com/user-attachments/assets/71bcf8a8-7211-44c8-ac41-4e6c2bc20c8d" />



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

<img width="782" height="79" alt="2" src="https://github.com/user-attachments/assets/b679c5ce-b410-47cb-8e20-a2cad217930e" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="782" height="79" alt="3" src="https://github.com/user-attachments/assets/2183b0f9-b565-456d-a347-2d33a2e732f1" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="782" height="171" alt="4" src="https://github.com/user-attachments/assets/ea06a9f2-c7ab-4f97-adaa-8d527214d890" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="782" height="171" alt="5" src="https://github.com/user-attachments/assets/9702c2bc-a503-43c0-b008-7180a87d3c8c" />



tar -xvf backup.tar
## OUTPUT

<img width="782" height="171" alt="6" src="https://github.com/user-attachments/assets/9b773880-d96d-4cf9-8d4b-e8be33a7dccc" />



gzip backup.tar

ls .gz
## OUTPUT

<img width="782" height="42" alt="7" src="https://github.com/user-attachments/assets/ae7f5b45-e406-407b-a328-79b81276c367" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="782" height="42" alt="8" src="https://github.com/user-attachments/assets/8c85addc-560b-44f5-8555-1fbef81a4cda" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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

./ifnested.sh 
## OUTPUT



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
## OUTPUT


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
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

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
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
