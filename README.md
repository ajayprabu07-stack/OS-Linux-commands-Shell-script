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
<img width="1207" height="741" alt="image" src="https://github.com/user-attachments/assets/56c50db5-b812-4e25-9f12-7c9dd777d136" />



cat < file2
## OUTPUT
<img width="1446" height="722" alt="image" src="https://github.com/user-attachments/assets/5d262398-8e75-4448-9d07-74cbe3ae7abc" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="1457" height="740" alt="image" src="https://github.com/user-attachments/assets/e2605f64-c27b-4c82-ab91-931ba39ee428" />

comm file1 file2
 ## OUTPUT
<img width="1457" height="731" alt="image" src="https://github.com/user-attachments/assets/3328fda3-93d8-4592-873a-c212513d1c37" />

 
diff file1 file2
## OUTPUT
<img width="1452" height="742" alt="image" src="https://github.com/user-attachments/assets/b86984aa-ea5a-481a-bea7-d65fe855ea03" />


# Filters

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
<img width="1480" height="732" alt="image" src="https://github.com/user-attachments/assets/099c70e9-5634-4059-8188-042b45b4fd31" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="1500" height="756" alt="image" src="https://github.com/user-attachments/assets/c3751734-8e0d-4f43-8697-63c4aff8397e" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="1467" height="750" alt="image" src="https://github.com/user-attachments/assets/9e73806b-ba9e-4a18-a1e5-a97d4571ff8d" />


cat > newfile 
```
Hello world
hello world
^d
````
 
grep Hello newfile 
## OUTPUT
<img width="1472" height="590" alt="image" src="https://github.com/user-attachments/assets/9c27cd89-43ad-43d1-919c-c077197f3553" />



grep hello newfile 
## OUTPUT
<img width="1217" height="567" alt="image" src="https://github.com/user-attachments/assets/278beb44-5688-4bf7-9672-1bb6a0a771d1" />




grep -v hello newfile 
## OUTPUT

<img width="1215" height="552" alt="image" src="https://github.com/user-attachments/assets/519436c9-f2a3-40c7-b941-6ca13905c1bd" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="1267" height="542" alt="image" src="https://github.com/user-attachments/assets/43f775ef-e3ec-45c3-9120-d7095eb9dd89" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="832" height="531" alt="image" src="https://github.com/user-attachments/assets/d1584340-55be-4286-ac6b-d951f9ce29e7" />



grep -R ubuntu /etc
## OUTPUT

<img width="1447" height="761" alt="image" src="https://github.com/user-attachments/assets/fecbe5bc-3956-4e61-b91b-e90e706e3f20" />


grep -w -n world newfile   
## OUTPUT
<img width="1427" height="506" alt="image" src="https://github.com/user-attachments/assets/c3e0f48e-d228-4f03-9557-bf5a74372b4e" />


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

<img width="1357" height="527" alt="image" src="https://github.com/user-attachments/assets/4f85fdbf-b620-4217-9291-7d74b19b313e" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1161" height="592" alt="image" src="https://github.com/user-attachments/assets/c34dd799-fca2-4a80-91d0-65c07baf73d4" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1002" height="595" alt="image" src="https://github.com/user-attachments/assets/bb716dd6-2137-4353-b0d7-107c15450cb8" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="852" height="582" alt="image" src="https://github.com/user-attachments/assets/fe51c9f6-daa6-447d-a359-f4b7408ba1ea" />



egrep '(world$)' newfile 
## OUTPUT

<img width="1036" height="565" alt="image" src="https://github.com/user-attachments/assets/ce48ce32-a409-42af-80e3-3d5d2edd63b2" />


egrep '(World$)' newfile 
## OUTPUT
<img width="965" height="287" alt="image" src="https://github.com/user-attachments/assets/5f979669-1afd-474f-a311-afced5b5aeed" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1387" height="492" alt="image" src="https://github.com/user-attachments/assets/4d29adfa-066e-4c9f-973b-420ee9c463af" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1212" height="505" alt="image" src="https://github.com/user-attachments/assets/0f4959fc-4a29-47ce-a76b-9cfa82c8dee5" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1291" height="607" alt="image" src="https://github.com/user-attachments/assets/e7a63a13-6b6d-4419-8be4-2c5eee59b8bb" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1002" height="205" alt="image" src="https://github.com/user-attachments/assets/da56d5d4-f738-4446-99d2-a872bdbb9f12" />


egrep l{2} newfile
## OUTPUT
<img width="791" height="110" alt="image" src="https://github.com/user-attachments/assets/374a9016-8d81-4a2c-a61d-382c229da6ae" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="747" height="180" alt="image" src="https://github.com/user-attachments/assets/111656c8-e527-414e-8f32-f1133d86ee8e" />


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
<img width="801" height="502" alt="image" src="https://github.com/user-attachments/assets/79ac84e2-eddf-478e-9eef-75b1b8186ffd" />



sed -n -e '$p' file23
## OUTPUT
<img width="1040" height="527" alt="image" src="https://github.com/user-attachments/assets/89ef6384-c1a6-4787-9d3a-8ce3598067fc" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1292" height="442" alt="image" src="https://github.com/user-attachments/assets/495d5842-79d1-46df-85f4-f37fc9184980" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="787" height="275" alt="image" src="https://github.com/user-attachments/assets/cd750d72-e6d5-48ca-aaa9-3d11d7d2815f" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="741" height="255" alt="image" src="https://github.com/user-attachments/assets/945d4c2a-72d0-4ce1-a4d2-0b6bf7ecd266" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="605" height="170" alt="image" src="https://github.com/user-attachments/assets/00101b4c-eed7-42fe-b013-7227f86e02c7" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="742" height="127" alt="image" src="https://github.com/user-attachments/assets/a18f1e2f-1ea1-49e5-83b0-238f7f991c74" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="687" height="87" alt="image" src="https://github.com/user-attachments/assets/15704b82-07ee-4d92-b2a1-16cca5d90f8d" />



seq 10 
## OUTPUT

<img width="727" height="325" alt="image" src="https://github.com/user-attachments/assets/6dccf169-3cb3-400d-a0ec-ca1305539d36" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="655" height="142" alt="image" src="https://github.com/user-attachments/assets/c7bae069-14d8-4850-99d8-fcbda0c2a098" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="682" height="152" alt="image" src="https://github.com/user-attachments/assets/69685801-8fc6-40e7-af8b-4fce90b5b3b4" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="662" height="146" alt="image" src="https://github.com/user-attachments/assets/dfe1493e-6893-48a4-9b86-d54ba9157d06" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="642" height="125" alt="image" src="https://github.com/user-attachments/assets/dc4699a8-1590-42ae-a15c-6f1466bb1c6c" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="655" height="115" alt="image" src="https://github.com/user-attachments/assets/bbd7e3d0-87fb-4f95-b45b-8654704c7a48" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="687" height="120" alt="image" src="https://github.com/user-attachments/assets/fb71c3cb-31dd-44c5-9a5b-043736f913bf" />



sed -n '2,4{s/$/*/;p}' file23
<img width="757" height="112" alt="image" src="https://github.com/user-attachments/assets/71c4923c-a96b-4fdd-91f2-b139f661eab6" />


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
<img width="742" height="312" alt="image" src="https://github.com/user-attachments/assets/73f6317a-ffc3-4b41-9c7e-d71827b88cc4" />


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
<img width="887" height="342" alt="image" src="https://github.com/user-attachments/assets/e632f033-fb05-4b10-bede-a9a300c746b4" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="967" height="271" alt="image" src="https://github.com/user-attachments/assets/c6dedd97-49f2-4007-b312-320786d9fc27" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="997" height="327" alt="image" src="https://github.com/user-attachments/assets/3066777a-b13b-45f1-a266-952ab4d718a0" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="865" height="220" alt="image" src="https://github.com/user-attachments/assets/9ce84abc-41d9-47f4-b7fb-219b46f323b8" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="806" height="382" alt="image" src="https://github.com/user-attachments/assets/732c3c11-284f-4663-be3f-bdc9353644ac" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="785" height="317" alt="image" src="https://github.com/user-attachments/assets/ccc0ddcf-1956-4dc1-a6ff-7379b4e2c2b1" />


tar -xvf backup.tar
## OUTPUT
<img width="740" height="232" alt="image" src="https://github.com/user-attachments/assets/6f36249d-5e0b-4637-9042-39b4a1a6427e" />


gzip backup.tar
ls .gz
## OUTPUT
<img width="737" height="260" alt="image" src="https://github.com/user-attachments/assets/591f7654-828c-40e3-be9f-4c2b16ffa2b5" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="842" height="116" alt="image" src="https://github.com/user-attachments/assets/37f1f4ce-8804-4f4e-9310-045e6344437d" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="925" height="197" alt="image" src="https://github.com/user-attachments/assets/b3e6044d-cc84-469f-b2f5-ffabba794881" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="832" height="277" alt="image" src="https://github.com/user-attachments/assets/95f1eb21-6d71-45be-907c-e1cd3f01f8d9" />


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
<img width="1117" height="657" alt="image" src="https://github.com/user-attachments/assets/10f6648f-ed7f-4a7e-90ed-7fcb84def1ea" />

 
ls file1
## OUTPUT
<img width="672" height="72" alt="image" src="https://github.com/user-attachments/assets/0ca66e93-6036-4b3d-b431-b56e85a780fc" />

echo $?
## OUTPUT 
<img width="562" height="67" alt="image" src="https://github.com/user-attachments/assets/7ebca231-4b8c-43da-a064-ffa2ede8e5ab" />

 
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
## OUTPUT
<img width="847" height="281" alt="image" src="https://github.com/user-attachments/assets/efbe92cc-63fd-499f-90be-bb850460025b" />



chmod 755 strcomp.sh
./strcomp.sh 
## OUTPUT
<img width="675" height="132" alt="image" src="https://github.com/user-attachments/assets/65f8d7cb-b345-459f-a82a-66c5da71663b" />


# check file ownership
cat < passwdperm.sh 
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

cat passwdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./passwdperm.sh
## OUTPUT
<img width="730" height="102" alt="image" src="https://github.com/user-attachments/assets/c3e0813e-4dfa-4c75-bbb5-b3d70fad6b28" />

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
<img width="1016" height="567" alt="image" src="https://github.com/user-attachments/assets/3abc9a33-5b0b-4832-a9db-e4f43dc2be06" />



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
## OUTPUT
<img width="1091" height="466" alt="image" src="https://github.com/user-attachments/assets/1c824f6f-69b8-4ede-b97f-fed67235e8cc" />
# looking for a possible value using elif

cat > elifcheck.sh 

```
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

```
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
