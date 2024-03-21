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
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat < file2
## OUTPUT
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
# Comparing Files
cmp file1 file2

 
 ## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/b5b6a958-7648-461f-a09e-ef9810681f60)



comm file1 file2

## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/b0ea0108-5402-47fb-b850-a5495c2fee4e)



diff file1 file2


##OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/5f458e1f-37e3-44c4-8b40-a36aadc2ee30)



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

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/49b04fc8-603d-4f3f-b14f-51f8e593d96c)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/3c3610d6-dfef-42ea-9480-a65100d45017)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/52fd145e-f17b-42d5-8206-e213b719c843)


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

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/ac2d4b33-19fb-4969-8ba9-754d985566ed)


grep hello newfile 
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/2aa97c12-16ce-4100-b1c8-7362fc6480ed)




grep -v hello newfile 
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/a565e9c9-c9b7-4a48-b434-c62597e2c986)


cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/53d407f2-55f7-48fb-8339-1437cd73a4b6)




cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/99f1e23d-1d19-42fe-971f-0f64a0b8349b)


grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/db151a2e-27b0-41c8-889a-635ea166b9b0)

grep -w -n world newfile   
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/ee843ab3-3aed-4b4b-8fab-52c9f82bb766)

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

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/a82bdf3c-e49d-4d6a-ae09-06b0db632ea8)


egrep -w '(H|h)ello' newfile 
## OUTPUT


![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/177be7db-bec7-4c15-8668-2f71f8673974)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/7a9e9f11-eb5b-4eb6-8782-16e5917064f2)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/1f622eba-3fd8-4d07-8648-2104cfdb3368)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/334a4fc2-e4b2-4f72-b813-3e2031da52de)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/0b3f8d54-ef71-4790-a7b4-a1860f1cceb3)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/8effb5d5-f25c-4326-a1f2-faf17e3f81d2)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/ee17463b-11a2-4fce-8b90-d109e4aa1e25)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/4cc6c7a4-a4cb-4703-982a-1142a0e0b9fd)


egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/75454366-ffb0-4834-bb01-d0f6d084664d)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/e606388a-9334-4fc5-9a48-a9f365f8f8d2)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/285a3119-c862-46c2-b7a1-8faa6fe0bafb)


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
![304757591-a648b63d-4908-491b-83e2-15d2a6549860](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/6067006c-52ab-4263-bb7c-8675a5cba9d7)



sed -n -e '$p' file23
## OUTPUT
sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/5febfd83-a054-4306-a391-158144c490df)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/40f1d1a6-6917-4d7f-8a0a-e405bb274637)

sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/b050a3fb-37c1-49df-b369-b53f685e33fc)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/b7e50c9d-4dfa-4db0-bf1c-a8aaf54867d2)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![304759889-30234a9f-dd11-4ae5-b7a5-9045148072a0](https://github.com/23004513/OS-Linux-commands-Shell-script/assets/138973069/ca6da655-591e-498b-9afb-e9bcd8e09c64)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/c2fa87bb-7bca-4d85-9707-f46572c774b7)



seq 10 
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/1042651d-773c-485f-a8c1-fb5392546aa5)


seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/c3cbbf19-7d40-4c77-b58c-f204bed64fd5)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/ab38125e-0664-4251-a571-7cc424febb6f)


seq 3 | sed '2a hello'
## OUTPUT


![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/661ae948-e054-4622-aefb-f8f5253c3af7)

seq 2 | sed '2i hello'
##OUTPUT


![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/c59c5039-2e76-4360-b1e8-372e2690dad8)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/351a6eeb-60d0-4109-bf7e-b34e83b78b5a)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/480eb84d-9577-40ed-be0b-513ccd3a50ce)

sed -n '2,4{s/$/*/;p}' file23
##OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/e957d8ac-4cc8-41b4-931c-bcdcc8ea9f7e)


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

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/14a29545-e650-4a46-aed6-26416ee902f3)

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


![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/48511b27-22ea-4ed6-a6e6-082a59e865e1)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/862bab50-e9d2-4e14-ad1b-2f2c197b896a)

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


![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/fbffe2bb-0cea-4f2c-afab-e93b6edb937e)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/37532572-b213-48c3-ad3a-f4e7d9a0c6e2)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/Nishanth-018/OS-Linux-commands-Shell-script/assets/149347651/c1bb3a09-2e7d-4f04-908e-6419145b07b3)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
tar -xvf backup.tar
## OUTPUT
gzip backup.tar
ls .gz
## OUTPUT
 gunzip backup.tar.gz
## OUTPUT

 
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
