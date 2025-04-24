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
![WhatsApp Image 2025-04-24 at 03 04 35_0bdf1089](https://github.com/user-attachments/assets/650a0b35-7566-452c-8ce9-7d6e39e84b17)

cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/5eda2a26-b6c3-4685-9c36-02ae40cfd7a4)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/bd80eccd-f2f3-475c-8586-993e51eef3a7)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/6fe54222-dd96-45e3-be33-c807a6276d43)

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/01528c41-ed90-4041-bc58-83c36c147887)

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
![WhatsApp Image 2025-04-24 at 03 04 33_6f2627ea](https://github.com/user-attachments/assets/b1ff8748-eaa9-4e2f-a4b7-62a0b3096843)




cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/39cd02c2-1b70-4653-9421-1c4c7abca4cd)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/d799a268-8cb7-47ff-bea4-37b2eb4248aa)


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
![WhatsApp Image 2025-04-24 at 03 04 33_6867c443](https://github.com/user-attachments/assets/86af938e-74de-4aa2-9ab8-910ce64b787f)



grep hello newfile 
## OUTPUT
![WhatsApp Image 2025-04-24 at 03 04 33_6e81ee1f](https://github.com/user-attachments/assets/2d22eef3-b5c7-4b26-8ffd-662fea3c73b4)




grep -v hello newfile 
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 33_5a05236b](https://github.com/user-attachments/assets/b0dd8cc1-c4df-4dde-af6c-c9bd396537cb)


cat newfile | grep -i "hello"
## OUTPUT
![WhatsApp Image 2025-04-24 at 03 04 33_c4105ae6](https://github.com/user-attachments/assets/ef573b23-1aa6-4423-a7d6-cabf83d299cc)




cat newfile | grep -i -c "hello"
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 33_b1ff876e](https://github.com/user-attachments/assets/a976e455-e858-4f0e-9d89-dfc8660e493b)



grep -R ubuntu /etc
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 33_d5771109](https://github.com/user-attachments/assets/852199be-98be-4a5b-aebc-6aaa5980f76b)


grep -w -n world newfile   
## OUTPUT
![WhatsApp Image 2025-04-24 at 03 04 34_d7852806](https://github.com/user-attachments/assets/6a6a6ed8-146e-4bcc-8482-f415564cb164)


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

![WhatsApp Image 2025-04-24 at 03 04 34_2a142a0b](https://github.com/user-attachments/assets/91b169a2-c411-4568-b222-96bcebaea439)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![WhatsApp Image 2025-04-24 at 03 04 34_14d1d0d9](https://github.com/user-attachments/assets/dbc4c638-9e73-4faa-a225-369d6b15242a)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 34_ede03ad6](https://github.com/user-attachments/assets/dd2d8ef0-cd1d-4b08-9df9-613be4bf5237)



egrep '(^hello)' newfile 
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 35_539b8de7](https://github.com/user-attachments/assets/021f45c7-57e3-4d35-b36d-cae9d07431ea)


egrep '(world$)' newfile 
## OUTPUT
![WhatsApp Image 2025-04-24 at 03 04 35_1f315e62](https://github.com/user-attachments/assets/3e5f4665-0afd-4cf9-a771-667e04114870)



egrep '(World$)' newfile 
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 35_0973e37e](https://github.com/user-attachments/assets/c2efcf97-2212-476d-803d-e68f04f43140)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 35_e9f00552](https://github.com/user-attachments/assets/6526239c-f52e-4abe-aa23-fb5192013c8a)


egrep '[1-9]' newfile 
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 35_11ca8707](https://github.com/user-attachments/assets/b7bda625-9f6a-4fd3-b473-e067220ff4ba)


egrep 'Linux.*world' newfile 
## OUTPUT
![WhatsApp Image 2025-04-24 at 03 04 35_cd29caee](https://github.com/user-attachments/assets/2d1f2616-f69f-4998-85e3-0789a4013952)


egrep 'Linux.*World' newfile 
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 35_ceebe69d](https://github.com/user-attachments/assets/c4c7a4fd-9975-46b0-b01b-da81cdbf13eb)


egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2025-04-24 at 03 04 35_6a2eb7e2](https://github.com/user-attachments/assets/ba9a4719-2072-4526-868a-15ae18a67b2e)


egrep 's{1,2}' newfile
## OUTPUT 
![WhatsApp Image 2025-04-24 at 03 04 35_d70fb6b4](https://github.com/user-attachments/assets/1c453f79-ac7b-464c-80c7-01c038a84c4c)


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

![WhatsApp Image 2025-04-24 at 03 04 35_9b309667](https://github.com/user-attachments/assets/a4ba6514-18be-42cf-a465-18b3d6db5798)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/e1a9e0a4-e1ec-49c3-82ef-b4c20532ab65)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/58f53e8d-3752-4117-bd85-47a2a371806f)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/4b4908e1-345f-4efa-9992-5773852dc3b2)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/f9b25691-e664-49d8-924c-01c9a9be4928)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/74396a1c-b85a-4d7a-949a-817793679929)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/a43db6ba-5805-42fa-8c94-1edecaaa1abe)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/168e71d2-f6b6-4f59-aec2-33e59ecd4fc7)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/c0bdfa44-5c1e-4602-8e7b-56e19a38ddb3)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/d90e9c1e-1f20-4594-a1b9-3548bd151dcb)



seq 10 | sed -n '2,~4p'
## OUTPUT

![image](https://github.com/user-attachments/assets/b8c2f338-7768-4e04-bc02-47be846012cf)


seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/cf0e1666-bb54-4b84-851b-5310c858c43c)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/84962504-39f1-4941-9031-36f235064aee)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/d4f4478d-29de-4c93-bb25-7063631b0bd0)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/657f4a74-f1a6-4e73-bfc2-62afd6cb0f93)


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

![image](https://github.com/user-attachments/assets/db25365c-67af-4303-af86-848ec15a0263)

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

![image](https://github.com/user-attachments/assets/0ec948dc-e048-4a71-931e-46441c058942)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/c906dec4-8661-480c-ae10-16d2bcf69ce5)

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

![image](https://github.com/user-attachments/assets/23c36cec-d677-4a94-ad6d-1d08ccbc8a95)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/5d89198d-c443-4ac6-9351-97df563d5f0a)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/c8da3839-fae1-46da-83fd-e87a955bc6cf)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/240b323c-4f17-4d6c-88a8-99d5dfa0e3a3)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/21a4c9a3-55d7-43df-b1f7-fa239d7bee31)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/05665336-906c-49bc-8c8f-7ec48590eb5c)

gunzip backup.tar.gz
## OUTPUT

 ![image](https://github.com/user-attachments/assets/357c7269-6899-4053-9fa9-9e06ee5e3894)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![image](https://github.com/user-attachments/assets/911d7d22-6216-4735-9bc9-a2676380c5f3)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/13b315f0-a4cc-4026-9fe0-40f627a12958)

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
![image](https://github.com/user-attachments/assets/dc65994c-5ef8-41cd-b3d3-ea01b9a0bfc9)

 
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
