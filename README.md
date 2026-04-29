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

<img width="223" height="163" alt="Screenshot 2026-04-26 132315" src="https://github.com/user-attachments/assets/62a342ef-0b38-4a85-9362-17decb258d13" />

cat < file2
## OUTPUT
<img width="249" height="105" alt="WhatsApp Image 2026-04-29 at 2 19 03 PM" src="https://github.com/user-attachments/assets/87dbd2f8-e30d-4bb8-9161-4c088b76319c" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="306" height="44" alt="image" src="https://github.com/user-attachments/assets/3fc9e361-0375-4614-8c65-ba5e3038011d" />

comm file1 file2
 ## OUTPUT
<img width="298" height="151" alt="WhatsApp Image 2026-04-29 at 2 21 27 PM" src="https://github.com/user-attachments/assets/23b8e764-5172-42f1-90b2-840f1289774b" />

 
diff file1 file2
## OUTPUT
<img width="297" height="198" alt="image" src="https://github.com/user-attachments/assets/6c94c824-24af-4176-8601-1becc421320d" />

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

<img width="247" height="64" alt="WhatsApp Image 2026-04-29 at 2 22 46 PM" src="https://github.com/user-attachments/assets/a7d59f6b-c41f-41d9-b210-172b89927534" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="308" height="76" alt="WhatsApp Image 2026-04-29 at 2 24 38 PM" src="https://github.com/user-attachments/assets/20b3826f-0e75-4c27-8d00-5e1cb93b960c" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="308" height="77" alt="WhatsApp Image 2026-04-29 at 2 25 15 PM" src="https://github.com/user-attachments/assets/a9bc056c-dd8e-400b-bb90-4db42e471f72" />


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

<img width="217" height="48" alt="WhatsApp Image 2026-04-29 at 2 27 46 PM" src="https://github.com/user-attachments/assets/dcdab27c-0ecd-41b8-a899-2bf3883604a7" />


grep hello newfile 
## OUTPUT

<img width="208" height="44" alt="WhatsApp Image 2026-04-29 at 2 28 45 PM" src="https://github.com/user-attachments/assets/c7845cf5-0e7c-4fb9-85cd-4be6607fed5b" />



grep -v hello newfile 
## OUTPUT

<img width="416" height="92" alt="WhatsApp Image 2026-04-29 at 2 29 26 PM" src="https://github.com/user-attachments/assets/ba126368-04ed-454c-9e57-282d01ab470a" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="416" height="61" alt="WhatsApp Image 2026-04-29 at 2 30 09 PM" src="https://github.com/user-attachments/assets/58394a8d-78f1-46bf-874b-44f4d461076f" />



cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="416" height="79" alt="WhatsApp Image 2026-04-29 at 6 26 44 PM" src="https://github.com/user-attachments/assets/a1fb5514-e2fe-4402-aac6-9827570c4189" />

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
<img width="380" height="60" alt="image" src="https://github.com/user-attachments/assets/3bf795be-5c12-4f6f-a6f2-da7c56ccad6a" />




egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="401" height="61" alt="WhatsApp Image 2026-04-29 at 6 29 53 PM" src="https://github.com/user-attachments/assets/aace6e39-b85a-4271-917e-e7f27e41b9e9" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="320" height="60" alt="WhatsApp Image 2026-04-29 at 6 31 08 PM" src="https://github.com/user-attachments/assets/3421f2c4-b67f-45dd-96a1-1b7092fe6f81" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="323" height="47" alt="WhatsApp Image 2026-04-29 at 6 32 27 PM" src="https://github.com/user-attachments/assets/4cbfed96-73e3-47bd-846b-40c7540f15f5" />


egrep '(world$)' newfile 
## OUTPUT

<img width="390" height="60" alt="WhatsApp Image 2026-04-29 at 6 33 45 PM" src="https://github.com/user-attachments/assets/98f22f7a-aa12-4d7e-b489-6b1d8aa075bc" />

egrep '(World$)' newfile 
## OUTPUT
<img width="328" height="48" alt="WhatsApp Image 2026-04-29 at 6 34 30 PM" src="https://github.com/user-attachments/assets/f98e1767-9660-4de1-9da3-99cf781eb9ee" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="536" height="79" alt="WhatsApp Image 2026-04-29 at 6 35 35 PM" src="https://github.com/user-attachments/assets/dfe7f610-8d12-4286-ac9b-8847c54e6b00" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="320" height="47" alt="WhatsApp Image 2026-04-29 at 6 36 37 PM" src="https://github.com/user-attachments/assets/2be66ebc-d3e1-44f3-9518-b80e606549e4" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="333" height="49" alt="image" src="https://github.com/user-attachments/assets/06918a3d-f5dd-4481-8911-e33e617d4670" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="326" height="48" alt="WhatsApp Image 2026-04-29 at 6 38 11 PM" src="https://github.com/user-attachments/assets/79b98b4f-fab7-457e-9b9e-f4c95cfb35ae" />

egrep l{2} newfile
## OUTPUT

<img width="414" height="61" alt="WhatsApp Image 2026-04-29 at 6 39 37 PM" src="https://github.com/user-attachments/assets/fa377de1-b902-4b9a-a40d-b22f09a5d8c2" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="488" height="77" alt="WhatsApp Image 2026-04-29 at 6 40 16 PM" src="https://github.com/user-attachments/assets/d5e66425-9dbe-4256-9f06-b6176df656a8" />


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



sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT



sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT



sed -n -e '1,5p' file23
## OUTPUT



sed -n -e '2,/Joe/p' file23
## OUTPUT




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT



seq 2 | sed '2i hello'
## OUTPUT


seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
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
<img width="470" height="106" alt="image" src="https://github.com/user-attachments/assets/b7d64ed8-ec82-47f1-9c2d-31298073b5ce" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="429" height="77" alt="image" src="https://github.com/user-attachments/assets/da812c4a-fecb-47d5-942c-8a8d1e69408a" />


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
<img width="546" height="270" alt="image" src="https://github.com/user-attachments/assets/17ad3903-f340-4c3b-992c-18e5117e5d6b" />

 
ls file1
## OUTPUT
<img width="316" height="54" alt="image" src="https://github.com/user-attachments/assets/232a900b-9536-482b-ac5b-75002b9aafed" />

echo $?
## OUTPUT 
<img width="165" height="46" alt="image" src="https://github.com/user-attachments/assets/4753b748-586d-4719-abff-fbbe7697a1ee" />

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
<img width="329" height="140" alt="image" src="https://github.com/user-attachments/assets/80155112-61ca-4fcf-ad20-ca0c5e6e353a" />


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
<img width="401" height="101" alt="image" src="https://github.com/user-attachments/assets/580c1dd2-536d-4497-9ef3-7047555661d1" />

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
<img width="532" height="105" alt="image" src="https://github.com/user-attachments/assets/e5df23ac-e64e-4d46-94a9-99ffd58d5737" />



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
<img width="277" height="114" alt="image" src="https://github.com/user-attachments/assets/376930f3-5587-416e-a3cc-6a99d9390a6e" />

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
<img width="532" height="105" alt="image" src="https://github.com/user-attachments/assets/e5df23ac-e64e-4d46-94a9-99ffd58d5737" />


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
<img width="274" height="127" alt="image" src="https://github.com/user-attachments/assets/536f41a6-6ad3-4ebc-a12c-aedf5378d693" />


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
<img width="445" height="121" alt="image" src="https://github.com/user-attachments/assets/164d2353-9bb1-46a5-bbb7-3d358ee9daae" />


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
 <img width="318" height="77" alt="image" src="https://github.com/user-attachments/assets/f6753082-a798-4f2b-ac19-87ff7ecbd03f" />

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
 <img width="348" height="156" alt="image" src="https://github.com/user-attachments/assets/b1556562-d17b-4bbd-a335-d4e0da3376d6" />

 
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
 <img width="363" height="152" alt="image" src="https://github.com/user-attachments/assets/32741e24-b0ac-46e6-b86d-da3726a017de" />

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
 <img width="363" height="152" alt="image" src="https://github.com/user-attachments/assets/be981bb8-8e14-410b-ac05-759b71ca6549" />

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
 <img width="243" height="156" alt="image" src="https://github.com/user-attachments/assets/5c79f832-309f-4b9c-85f8-366fbef09e6d" />

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
<img width="348" height="156" alt="image" src="https://github.com/user-attachments/assets/b1556562-d17b-4bbd-a335-d4e0da3376d6" />

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
<img width="270" height="138" alt="image" src="https://github.com/user-attachments/assets/9f5a2ad4-5ffb-4970-8ecc-f0e8d30209aa" />

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
<img width="280" height="145" alt="image" src="https://github.com/user-attachments/assets/99cbef3c-59fc-4be6-96a3-2b3f13b9c9bd" />

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

 <img width="350" height="247" alt="image" src="https://github.com/user-attachments/assets/08b1342b-a1f0-43e4-8e23-6d02e8fe0748" />

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
<img width="367" height="92" alt="image" src="https://github.com/user-attachments/assets/c2d8ef83-8ac4-416e-8c7a-f68956cf6b1e" />


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
<img width="367" height="92" alt="image" src="https://github.com/user-attachments/assets/5cc43b92-6d5e-4a66-96c9-32b093209b44" />

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
<img width="264" height="48" alt="image" src="https://github.com/user-attachments/assets/64e1c4d0-3bff-4d9b-9c26-e0f17380390a" />


 
 ./funcex.sh 1 2
<img width="251" height="55" alt="image" src="https://github.com/user-attachments/assets/e189baba-75b7-495d-95f7-badfb2777e6b" />

 
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
<img width="255" height="113" alt="image" src="https://github.com/user-attachments/assets/ccac2000-3e27-41d3-bf85-b9f76565caf6" />


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
 <img width="286" height="83" alt="image" src="https://github.com/user-attachments/assets/1757bf65-17d0-44ce-9a70-20a42cd277f5" />

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
 
<img width="309" height="253" alt="image" src="https://github.com/user-attachments/assets/4266f82a-b8ff-4028-b414-fe93baffe6fa" />

 
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
 <img width="366" height="236" alt="image" src="https://github.com/user-attachments/assets/a0a6224d-0476-4d2d-82b2-10d6c022da9a" />

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
<img width="288" height="161" alt="image" src="https://github.com/user-attachments/assets/e5ce7371-a218-40e2-b313-237a6bd1eb68" />


# RESULT:
The Commands are executed successfully.
