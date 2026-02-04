 OS-Linux-commands-Shell-scripting
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
<img width="300" height="89" alt="image" src="https://github.com/user-attachments/assets/f7358d0b-9442-44d5-8f91-a5f55a1aeab0" />



cat < file2
## OUTPUT
<img width="321" height="135" alt="image" src="https://github.com/user-attachments/assets/015baedd-76a3-4cd2-bebe-ee28ee619f8c" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="362" height="44" alt="image" src="https://github.com/user-attachments/assets/0f4472f1-906a-4960-9f71-f92e3cf7853f" />

comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="image" src="https://github.com/user-attachments/assets/78482dda-0f90-4ceb-9c09-12791e3b7e1e" />

 
diff file1 file2
## OUTPUT
<img width="402" height="248" alt="image" src="https://github.com/user-attachments/assets/94425d2e-d01e-483d-9c2c-71aafe8f7463" />


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
<img width="325" height="77" alt="image" src="https://github.com/user-attachments/assets/48a29c47-46bb-4ff6-b099-3b52a916b81c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="367" height="96" alt="image" src="https://github.com/user-attachments/assets/7ce6dc04-9f85-4685-b6cd-595abd565093" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="371" height="95" alt="image" src="https://github.com/user-attachments/assets/15b438f7-00af-47e5-9642-20000c9e97c8" />


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
<img width="365" height="50" alt="image" src="https://github.com/user-attachments/assets/130898ca-551e-45b1-b698-26148cfae9b3" />



grep hello newfile 
## OUTPUT
<img width="366" height="51" alt="image" src="https://github.com/user-attachments/assets/11ad23a9-b177-4cfc-b84a-89234bc79320" />





grep -v hello newfile 
## OUTPUT
<img width="373" height="57" alt="image" src="https://github.com/user-attachments/assets/e22cf7b7-829d-4bc2-871a-326a0bb42a70" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="471" height="72" alt="image" src="https://github.com/user-attachments/assets/72da5959-c8f3-45cd-b56c-b13f64057db2" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="491" height="54" alt="image" src="https://github.com/user-attachments/assets/e4270e72-5918-4b8e-a126-7277c54e1435" />





grep -R ubuntu /etc
## OUTPUT

<img width="567" height="180" alt="image" src="https://github.com/user-attachments/assets/781648fe-d675-4f68-b356-c5f5d07db6c6" />


grep -w -n world newfile   
## OUTPUT
<img width="564" height="73" alt="image" src="https://github.com/user-attachments/assets/19ad36c2-258b-4a4c-a471-e3861dfb95b7" />


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
<img width="533" height="79" alt="image" src="https://github.com/user-attachments/assets/6c13a03f-57bd-4332-991e-7d789ce43dee" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="541" height="70" alt="image" src="https://github.com/user-attachments/assets/9012d49b-0f32-41e5-aac7-98dfabc705e1" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="538" height="75" alt="image" src="https://github.com/user-attachments/assets/9439c2b7-d245-483d-a2b3-64c81b30cb13" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="538" height="75" alt="image" src="https://github.com/user-attachments/assets/c038ed4b-b117-4b4a-8e34-37379c8d9efd" />


egrep '(world$)' newfile 
## OUTPUT


<img width="541" height="60" alt="image" src="https://github.com/user-attachments/assets/71e1bd01-c500-400c-bd82-817f42111658" />


egrep '(World$)' newfile 
## OUTPUT
<img width="541" height="54" alt="image" src="https://github.com/user-attachments/assets/ebebec51-b48e-4de7-a0b9-a3e7eee412b2" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="543" height="75" alt="image" src="https://github.com/user-attachments/assets/f40067e3-e8a6-4fef-baf7-763575336e6f" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="545" height="57" alt="image" src="https://github.com/user-attachments/assets/b34b21b5-ee03-4d3f-83b2-f62952984cd1" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="545" height="57" alt="image" src="https://github.com/user-attachments/assets/715dfda7-f235-4e2a-87fd-50f3543eb944" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="545" height="57" alt="image" src="https://github.com/user-attachments/assets/2e71fe89-345e-40c7-b84e-285933db9fab" />


egrep l{2} newfile
## OUTPUT
<img width="549" height="76" alt="image" src="https://github.com/user-attachments/assets/c637ca8d-41be-4532-be3b-960dffb10ad4" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="381" height="52" alt="image" src="https://github.com/user-attachments/assets/80132957-06a2-42fe-bf09-596a62c1a3df" />


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
<img width="545" height="97" alt="image" src="https://github.com/user-attachments/assets/37c7d205-5be4-443b-86e5-b4b0ca321e94" />



sed -n -e '$p' file23
## OUTPUT
<img width="428" height="49" alt="image" src="https://github.com/user-attachments/assets/3ba21703-7316-4dda-bf55-1b14a5b4295e" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="424" height="200" alt="image" src="https://github.com/user-attachments/assets/97863b9e-7293-4c7b-af84-a55ef52fbedc" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="424" height="200" alt="image" src="https://github.com/user-attachments/assets/42662325-0283-4a5d-882b-2ed8d1f50b47" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="469" height="203" alt="image" src="https://github.com/user-attachments/assets/9d63e4ed-bd9b-45cf-86e6-0f46fb090d9a" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="470" height="139" alt="image" src="https://github.com/user-attachments/assets/eb82b939-b9ae-4c83-ab9b-835420b4eaad" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="469" height="93" alt="image" src="https://github.com/user-attachments/assets/55e944f2-20da-4b74-929a-dcc212196488" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="468" height="69" alt="image" src="https://github.com/user-attachments/assets/d38607c1-91cf-45cc-bacc-d574a552333d" />



seq 10 
## OUTPUT

<img width="470" height="241" alt="image" src="https://github.com/user-attachments/assets/cc046ed3-cb7e-4c36-8d7a-2edf232772c1" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/020d3bf3-cbae-40ac-97b9-1bd703749705" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/39e644f5-5151-4da1-aa79-eaaa94964c86" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="476" height="116" alt="image" src="https://github.com/user-attachments/assets/04401c36-1907-46a1-85cb-ac91ca38927f" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/4d299c22-83bd-4763-9d13-a68b356e77cd" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/2c243826-e98b-4f7f-84cc-b12fbcf20916" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/b1764efd-d153-4546-9a1e-770728a2ea8d" />



sed -n '2,4{s/$/*/;p}' file23

<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/16f5b5a5-4a14-4d7f-8031-a51377d12985" />


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
