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
![Screenshot 2025-05-08 185314](https://github.com/user-attachments/assets/c58491ae-172e-4eef-a2c3-51be15fbc236)



cat < file2
## OUTPUT
![Screenshot 2025-05-08 185333](https://github.com/user-attachments/assets/af5e2822-5e2b-4964-858d-25be8c13963d)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot 2025-05-08 185345](https://github.com/user-attachments/assets/b17fd518-8067-4c7d-a289-c8c43411e287)

comm file1 file2
 ## OUTPUT
![Screenshot 2025-05-08 185409](https://github.com/user-attachments/assets/1b53aac1-17c1-42fe-a5c4-47497c327f6c)

 
diff file1 file2
## OUTPUT
![Screenshot 2025-05-08 185430](https://github.com/user-attachments/assets/92e30e7f-110e-4299-a5b0-98c77bbf9ca0)


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

![Screenshot 2025-05-08 185447](https://github.com/user-attachments/assets/a4920324-c7af-41d6-86ac-36a1fc4b8022)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2025-05-08 185542](https://github.com/user-attachments/assets/feedaa83-8e02-4b2d-83c6-83928c17768b)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-05-08 185647](https://github.com/user-attachments/assets/7fd964a7-7db0-4b01-b473-a9608424e972)


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
![Screenshot 2025-05-08 185658](https://github.com/user-attachments/assets/49860a7d-7db5-4f5e-9673-26316a524ede)



grep hello newfile 
## OUTPUT

![Screenshot 2025-05-08 185707](https://github.com/user-attachments/assets/b68b6fd3-c194-4b03-ac95-fa3a86f58438)



grep -v hello newfile 
## OUTPUT
![Screenshot 2025-05-08 185715](https://github.com/user-attachments/assets/1a27d071-6d04-4d1e-99b4-66871705b8a0)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2025-05-08 185723](https://github.com/user-attachments/assets/cea37f31-76f3-448b-8958-07974b7e0d8d)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2025-05-08 185731](https://github.com/user-attachments/assets/685f96a8-7886-4c20-9df1-8181f18c10e8)




grep -R ubuntu /etc
## OUTPUT
![Screenshot 2025-05-08 185741](https://github.com/user-attachments/assets/87947c25-f257-44c8-a0fd-882ed3ec7cea)



grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-05-08 185749](https://github.com/user-attachments/assets/db20d605-13be-46ea-ac68-ae658816c058)


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
![Screenshot 2025-05-08 185814](https://github.com/user-attachments/assets/8f16abf5-c676-46cd-9bc9-55185a730231)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot 2025-05-08 185826](https://github.com/user-attachments/assets/e0b2fc73-83bf-47d8-ba66-fbc2481790e2)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2025-05-08 185834](https://github.com/user-attachments/assets/da85b1a5-a5ed-4456-ba05-31a6b33ab301)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2025-05-08 185843](https://github.com/user-attachments/assets/7007869f-44c5-4314-815e-960cf02db154)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot 2025-05-08 185853](https://github.com/user-attachments/assets/90c6c907-2293-4d19-a652-531254b06538)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2025-05-08 185905](https://github.com/user-attachments/assets/f56cc38b-0ff5-4c24-8016-2add366ad700)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2025-05-08 185917](https://github.com/user-attachments/assets/729be162-c91d-49b5-a910-251bd0771e0c)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2025-05-08 185928](https://github.com/user-attachments/assets/4179cb59-15e6-48d7-b092-3c41c2481bce)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2025-05-08 185939](https://github.com/user-attachments/assets/03c279f5-2dbc-40a4-97ce-fd7afd386baa)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2025-05-08 190008](https://github.com/user-attachments/assets/2e0314b8-fc04-49d1-b11c-cc8c14cb0ed2)


egrep l{2} newfile
## OUTPUT

![Screenshot 2025-05-08 190020](https://github.com/user-attachments/assets/c5a69b45-f7f4-415e-936a-cdfa89515848)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2025-05-08 190029](https://github.com/user-attachments/assets/5af41516-32e8-479d-be2f-3a83d5e3fa82)


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
![Screenshot 2025-05-08 190039](https://github.com/user-attachments/assets/e5cd6d32-3727-4262-8846-86b4c4ea0a48)



sed -n -e '$p' file23
## OUTPUT
![Screenshot 2025-05-08 190050](https://github.com/user-attachments/assets/760459df-04ce-463b-9b67-d83c23b4d706)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-05-08 190056](https://github.com/user-attachments/assets/68c20b03-fbf1-4371-a844-98cb90a68647)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-05-08 190106](https://github.com/user-attachments/assets/156740e5-a74b-44aa-8cd9-e1b7481d1c62)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2025-05-08 190114](https://github.com/user-attachments/assets/b9e5acc0-4c2b-4b2a-aee3-824b4012e59c)



sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2025-05-08 190123](https://github.com/user-attachments/assets/53553778-a8a5-419d-b3ed-5e3aadc54a1c)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2025-05-08 190131](https://github.com/user-attachments/assets/2dd41c65-2e46-4846-849d-b56909b353b1)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot 2025-05-08 190141](https://github.com/user-attachments/assets/a5a68747-4a5e-4551-83ea-78a81058210d)



seq 10 
## OUTPUT
![Screenshot 2025-05-08 190148](https://github.com/user-attachments/assets/8c85f8ae-aae9-48bb-adeb-81f226633495)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot 2025-05-08 190155](https://github.com/user-attachments/assets/48cfa05c-e93c-4d9e-8158-10aac793af2f)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2025-05-08 190204](https://github.com/user-attachments/assets/cf280cb8-542e-40b2-ac33-3476bcb2828c)



seq 3 | sed '2a hello'
## OUTPUT

![Screenshot 2025-05-08 190212](https://github.com/user-attachments/assets/87711a6d-a42f-40a9-a997-805c19df06ab)



seq 2 | sed '2i hello'
## OUTPUT

![Screenshot 2025-05-08 190220](https://github.com/user-attachments/assets/23887e3c-9046-4c29-a33c-f42d11620e54)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2025-05-08 190236](https://github.com/user-attachments/assets/98b938ed-143c-42a7-92f0-526f1d106141)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot 2025-05-08 190332](https://github.com/user-attachments/assets/a5175c38-26d0-4426-bea7-6a2dea5da94a)



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

![Screenshot 2025-05-08 190339](https://github.com/user-attachments/assets/cd02a9bd-8fc5-45b1-a63f-87ef92515f14)


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

![Screenshot 2025-05-08 190349](https://github.com/user-attachments/assets/d8d87606-b572-4970-8cb4-e38bb29a06cf)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![Screenshot 2025-05-08 190359](https://github.com/user-attachments/assets/c0994db9-8a19-4d76-86ea-fd746a18e793)

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

![Screenshot 2025-05-08 190412](https://github.com/user-attachments/assets/cc40f475-264e-45bd-a112-b5e1b3a2b7a8)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2025-05-08 190428](https://github.com/user-attachments/assets/2c6e7708-4a6f-49a4-bb7c-451151510484)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot 2025-05-08 190444](https://github.com/user-attachments/assets/ba317c77-3d37-4a67-ad52-27c96c52ece0)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![Screenshot 2025-05-08 190508](https://github.com/user-attachments/assets/ee198e68-f89e-40fe-9266-7af266ce6df5)


tar -xvf backup.tar
## OUTPUT

![Screenshot 2025-05-08 190521](https://github.com/user-attachments/assets/b4105bd8-d08f-4480-86fa-a382d40d1477)

gzip backup.tar

ls .gz
## OUTPUT

![Screenshot 2025-05-08 190532](https://github.com/user-attachments/assets/1fb0e61f-1f0a-41d3-9df8-7cea5653a5e8)
 
gunzip backup.tar.gz
## OUTPUT

![Screenshot 2025-05-08 190544](https://github.com/user-attachments/assets/62107c73-53f0-4582-9d5c-a609e9c9796e)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![Screenshot 2025-05-08 190554](https://github.com/user-attachments/assets/d2a8a50d-de93-40d2-98ad-2e2dadd3cd37)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot 2025-05-08 190608](https://github.com/user-attachments/assets/410b594f-8661-4b0f-973d-cdf66adc566b)


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

![Screenshot 2025-05-08 190618](https://github.com/user-attachments/assets/ada1d5c0-0a2d-467c-b146-e83be525b6bb)

 
ls file1
## OUTPUT
![Screenshot 2025-05-08 190629](https://github.com/user-attachments/assets/d699ee1a-108d-4269-ac61-259b8fbb0b80)

echo $?
## OUTPUT 
![Screenshot 2025-05-08 190640](https://github.com/user-attachments/assets/c82d6ae1-6199-43d6-bb9b-d3bfea61db3b)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![Screenshot 2025-05-08 190649](https://github.com/user-attachments/assets/81818eb0-4cfe-44c3-9756-f661a8f449a7)

abcd
 
echo $?
 ## OUTPUT
![Screenshot 2025-05-08 190701](https://github.com/user-attachments/assets/cd681a3f-3f0f-4515-bbdd-b30ee23e1be5)


 
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
![Screenshot 2025-05-08 190715](https://github.com/user-attachments/assets/1e32edd2-c498-4cdb-9c59-b3f3756284cc)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot 2025-05-08 190728](https://github.com/user-attachments/assets/a4ff1935-7f54-42af-bf24-5132ce54d14b)


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
![Screenshot 2025-05-08 190741](https://github.com/user-attachments/assets/ad465daf-bd63-4c61-ae55-29904f7c782a)

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
![Screenshot 2025-05-08 190754](https://github.com/user-attachments/assets/af13c529-0419-4fb3-bcb9-c1c5cf4b9eed)



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
![Screenshot 2025-05-08 190804](https://github.com/user-attachments/assets/3acbce6f-19d0-46d9-a16b-f1cdec39ad5a)

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
![Screenshot 2025-05-08 190815](https://github.com/user-attachments/assets/29da963d-3388-4d5f-bdd8-18974cde58b2)

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
![Screenshot 2025-05-08 190825](https://github.com/user-attachments/assets/39ec8027-ba70-4ad8-bcb5-13f257901154)


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
![Screenshot 2025-05-08 190835](https://github.com/user-attachments/assets/445113e0-e633-4abc-8b82-3436c122ce8a)

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
![Screenshot 2025-05-08 190848](https://github.com/user-attachments/assets/af28104a-22bb-42cb-94b5-057b54fbdeee)

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
![Screenshot 2025-05-08 190858](https://github.com/user-attachments/assets/96eae11e-a5cf-444b-8974-ad61fd9b9326)


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
![Screenshot 2025-05-08 190953](https://github.com/user-attachments/assets/143ff127-323f-4255-8153-8f6d9bbf4832)


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
![Screenshot 2025-05-08 191001](https://github.com/user-attachments/assets/dd81d813-14ce-43d8-b264-ec37d803c61d)


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
![Screenshot 2025-05-08 191011](https://github.com/user-attachments/assets/a5bbdbf8-efa4-4856-8183-ba33bcc832bc)



 
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
![Screenshot 2025-05-08 191030](https://github.com/user-attachments/assets/faed8dfd-b8f5-43ef-9a05-3d1953455f90)



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
![Screenshot 2025-05-08 191038](https://github.com/user-attachments/assets/8671468f-8351-4e3d-b819-bba292042b3c)


 
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
![Screenshot 2025-05-08 191050](https://github.com/user-attachments/assets/abaf6a86-e779-48a5-b036-8e573c33f6fe)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![Screenshot 2025-05-08 191101](https://github.com/user-attachments/assets/8d8a0142-a7cc-4165-b0f6-205f5cb84249)



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
![Screenshot 2025-05-08 191111](https://github.com/user-attachments/assets/7051690c-c2d0-441b-92cd-407fc53be49c)


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

![Screenshot 2025-05-08 191111](https://github.com/user-attachments/assets/634e04a3-99cc-4bbf-aae2-75ab124034a1)
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
![Screenshot 2025-05-08 191111](https://github.com/user-attachments/assets/634e04a3-99cc-4bbf-aae2-75ab124034a1)

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
![Screenshot 2025-05-08 191121](https://github.com/user-attachments/assets/8138aafd-3e0a-4775-9665-ee2f21d62dbd)


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
![Screenshot 2025-05-08 191131](https://github.com/user-attachments/assets/f75fba6e-905b-462c-a74f-220e2547c856)
 
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

![Screenshot 2025-05-08 191139](https://github.com/user-attachments/assets/308534b1-68f9-4c1c-95a7-1a32d203313f)
# RESULT:
The Commands are executed successfully.
