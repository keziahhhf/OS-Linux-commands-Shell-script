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
![image](https://github.com/user-attachments/assets/ad6b6ba3-dafb-4893-ae22-c32368a2f55a)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/6c8e4138-a001-4cf5-ac62-69c7942dca54)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/3856b82f-77c7-4dcf-8df0-62f83c65df63)

comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/49b95d7a-fbcb-454d-8913-ffc038af6e21)

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

![image](https://github.com/user-attachments/assets/0760d3db-4f59-4a22-a039-bdb4ac10268b)



cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/79c28692-3a7d-401a-b41e-9574889231b5)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/a393bbf1-27db-494f-996d-e00c4a589ef0)


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
![image](https://github.com/user-attachments/assets/cf416ec2-c419-470b-acce-cd8501c3be9a)



grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/41653ea6-2b6e-4fc7-bf26-ca90bd3d3f71)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/9dc41556-b917-41be-85fa-b4f83085993f)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/9d58179c-b7ee-4219-84c8-8a888679d53d)



cat newfile | grep -i -c "hello"
## OUTPUT


![image](https://github.com/user-attachments/assets/f05b165a-fe75-46ca-9c52-95e7c0b6e215)


grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/ffac3451-57c0-4c5a-a80c-521ec5fc92f5)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/b52a7b22-2894-4d13-b899-8e7268b51c78)


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
![image](https://github.com/user-attachments/assets/cd31f805-2236-4aad-874b-e1b88a77f567)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/db9b9355-5fcd-4f4f-aa7b-3e9882f9a152)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/4a72b821-7b03-48ad-ac5d-7f4e91272809)




egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/80f7bd00-e2b6-44ad-96ac-5bc834721368)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c1829f48-4bcb-4b47-b260-eabf19f8d661)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/551db0cd-260e-4d29-805b-06bcd713788d)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/bcf501a7-db6a-468d-b667-76babd8dd9da)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/bc3ed6bf-7174-44f4-8ecd-27cfe6a0cfa1)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4ca85b32-0403-4a3d-b267-ea18167ef58c)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f1fc7a14-31a1-4fe2-8a26-dcd79ed7ffe2)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/aef795ad-0257-4ae3-957b-1ad69fcb9eb7)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/1ebacd16-3888-4b98-b212-8abeb080ec87)


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

![image](https://github.com/user-attachments/assets/7fad9b25-123e-442b-bd57-e336f23cfc62)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/49b59755-d1f7-4eff-b7f9-513124292148)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/0f648876-f8f2-40e0-8440-d035b0694c2b)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/b7cbd2b2-95ad-4d61-8fbc-bdaaec09dca6)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/d0a31245-6bd0-4355-892e-67a904360274)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/e1d413e2-94b5-48c2-a23f-91a75da9e8c5)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/3f59b8ff-c401-43ae-93c2-87a67a7a2431)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/0151f305-a52b-4edc-97cb-cf1104c2a7e4)


seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/e7189b42-d992-4ba4-9700-7603034c014a)



seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/user-attachments/assets/595a14d5-2cd9-490f-9b84-ee6f7885a4bb)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/617f6451-cb9c-4297-ae8f-6755ae96d4a4)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/b8d03de1-0373-45a6-85f1-06e3f0d72af1)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/9b868352-d079-4734-8e23-b64f31459d6a)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/d7848698-b836-4bff-9e8b-3c7c99785f1b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/4889f9fc-fdf1-45a5-ac0d-4508e6a3c6c6)



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/9ebf1f9a-939d-44d3-8e09-a477c47af2aa)


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
![image](https://github.com/user-attachments/assets/25228fc0-0d1a-4c7b-93cd-f28cb3c0f0d7)


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

![image](https://github.com/user-attachments/assets/4da63d3b-6c05-4b4b-88c5-c63a989b74fd)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/05ac2551-1302-44bd-88e3-d9423bcd044b)

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
![image](https://github.com/user-attachments/assets/1be002c8-6e0e-4a6b-8576-fb1aeb5740cb)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/0b17b427-820a-48a0-9cac-4890dee90ea3)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/b37816f1-d041-46a8-8f6e-b7ef8118b0dc)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/db700c14-5c3b-493c-9d6e-eaddf5912a00)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/2f8fdf36-a3be-4865-a225-67e2c4f47cac)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/c20890c5-d91e-4bc3-9979-d4a5a97b5c66)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/7ceba2af-5862-4c1e-8332-16a3e5a5b5be)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/97af7b75-bca7-426e-b9ef-60a56a592397)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/86520200-64f5-4e11-8437-e11c5ddf08bc)


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
![image](https://github.com/user-attachments/assets/568f59e3-f3fe-4d5d-8db4-053d6e0fd1b6)

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/31418ee7-7a00-4289-841e-e3af20e639d6)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/dd2a63da-be34-439d-a830-472b8cffc97a)

abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/89f604fc-57f6-4c5b-9b14-6608c80d05d2)


 
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
![image](https://github.com/user-attachments/assets/b1f2f684-0394-4ea4-8766-d8f7d63ec600)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/9ae23610-bd03-40a5-b213-a92393ea8b6c)


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
![image](https://github.com/user-attachments/assets/fba069a7-6969-4b92-9978-7f54c67e0067)

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

![image](https://github.com/user-attachments/assets/9c95c216-dbd9-4af4-8ad0-0c814ad6c62d)


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
![image](https://github.com/user-attachments/assets/88d99483-9b4b-41b7-b62d-a46b946ef7bd)

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
![image](https://github.com/user-attachments/assets/4e03679d-bdb3-42cb-9fd4-d377b91eed00)

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
![image](https://github.com/user-attachments/assets/aab9a39b-188f-4142-8f8f-15fe95e81c15)


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
![image](https://github.com/user-attachments/assets/e47c0343-74c7-422c-bbde-5fb69a58a979)

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
## Output
![image](https://github.com/user-attachments/assets/49161cf6-928e-4ff8-87e5-533de102c5c0)

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
 
 ##Output
 ![image](https://github.com/user-attachments/assets/c7795e6a-2bdc-4a15-a59e-8207c8813291)

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
 
 ##Output
 ![image](https://github.com/user-attachments/assets/dcd595a0-388e-4c5a-ac07-88d8c3d45838)

 
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
 
##Output
![image](https://github.com/user-attachments/assets/e1f7efbb-1b79-4c93-bc27-a189b569026a)

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
 ##Output
 ![image](https://github.com/user-attachments/assets/47daf5dc-ef9b-4c29-a610-2a67ff65fece)

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
![image](https://github.com/user-attachments/assets/2d54f8ed-9722-410b-89c3-d16349840574)

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
##Output
![image](https://github.com/user-attachments/assets/9c59e510-7bfc-4058-ade3-59929cd2a3ff)

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![image](https://github.com/user-attachments/assets/627c67f7-afad-4411-91fd-a28a7b8a0002)


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
![image](https://github.com/user-attachments/assets/00796906-4f1d-4298-8ede-5d8190690d0e)


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
![image](https://github.com/user-attachments/assets/a9a3519b-430d-40be-a361-9dc9052e6c03)

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
![image](https://github.com/user-attachments/assets/c07c4911-15f7-47a4-b560-aab7a100d892)

 
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
![image](https://github.com/user-attachments/assets/8a989b74-d1cc-472d-b836-ba4f3c18e10b)

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
 ![image](https://github.com/user-attachments/assets/ddf2b977-5b0e-425f-b857-92b6b358c885)

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

![image](https://github.com/user-attachments/assets/76cb2ef4-05af-4c90-9e29-2dde6a642ec7)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/1da002da-c53d-4a76-9967-b26ef7419191)



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
![image](https://github.com/user-attachments/assets/be27deb5-6510-4b56-9472-5d09505d527a)

 
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
 ![image](https://github.com/user-attachments/assets/c35651bb-c7a5-4b54-898f-fc4569b1e81d)

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
 ![image](https://github.com/user-attachments/assets/c94d3f77-a7d2-442a-8bf8-f3505b1b799f)

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
 ![image](https://github.com/user-attachments/assets/d468f6bc-f80a-4869-811f-24ed89af37d8)

 
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
 ![image](https://github.com/user-attachments/assets/16e4dfb7-a72b-4aa2-a0ac-c991f93fcacf)

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
![image](https://github.com/user-attachments/assets/df60fef4-f38d-4d0c-9c27-5f25cbafcad3)


# RESULT:
The Commands are executed successfully.
