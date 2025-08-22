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
<img width="165" height="86" alt="image" src="https://github.com/user-attachments/assets/cde5abf3-0766-4c3f-ad66-105767a990ca" />



cat < file2
## OUTPUT
<img width="157" height="104" alt="image" src="https://github.com/user-attachments/assets/8c2ae495-1a3f-4a23-9ff8-034b5baa5547" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="271" height="36" alt="image" src="https://github.com/user-attachments/assets/03345e61-4640-47fe-aa30-dffce2fcfe68" />

comm file1 file2
 ## OUTPUT
<img width="294" height="181" alt="image" src="https://github.com/user-attachments/assets/38858ec5-9cf8-4f10-9853-0539f079f3ef" />

 
diff file1 file2
## OUTPUT
<img width="200" height="171" alt="image" src="https://github.com/user-attachments/assets/be3d1dc5-7a68-46d6-9dc3-8826bc34eb57" />


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
<img width="199" height="75" alt="image" src="https://github.com/user-attachments/assets/5c285bc7-1640-46f1-b958-92879d74eeeb" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="220" height="68" alt="image" src="https://github.com/user-attachments/assets/0475bdfa-c222-4898-af28-185612bb101b" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="201" height="95" alt="image" src="https://github.com/user-attachments/assets/99ba7273-4024-4e0d-8d68-1d3dbc8b922d" />


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
<img width="282" height="38" alt="image" src="https://github.com/user-attachments/assets/f4ac9d44-1368-4f55-b5ae-15626bfe60f8" />



grep hello newfile 
## OUTPUT
<img width="190" height="35" alt="image" src="https://github.com/user-attachments/assets/5ee793e9-d973-4266-aaa6-6142af11a5f4" />



grep -v hello newfile 
## OUTPUT
<img width="195" height="35" alt="image" src="https://github.com/user-attachments/assets/ad23fd0b-fcf2-4e0f-b0f5-77de1c1729fe" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="286" height="55" alt="image" src="https://github.com/user-attachments/assets/e59fc60c-3fab-4582-9613-ac58ee580a31" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="263" height="36" alt="image" src="https://github.com/user-attachments/assets/354bc121-0372-491b-9a61-79419217b442" />



grep -R ubuntu /etc
## OUTPUT
<img width="1289" height="446" alt="image" src="https://github.com/user-attachments/assets/6f81ef7e-02ee-460f-bab4-b8d0886fb5d1" />



grep -w -n world newfile   
## OUTPUT
<img width="217" height="50" alt="image" src="https://github.com/user-attachments/assets/02f43fce-5afd-4997-9ae8-74830601d56d" />


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
<img width="321" height="58" alt="image" src="https://github.com/user-attachments/assets/0aaedbb1-8568-40c2-8051-598f38053d75" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="258" height="73" alt="image" src="https://github.com/user-attachments/assets/fe39beb7-842a-4f26-a9a6-3242a903fb61" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="320" height="78" alt="image" src="https://github.com/user-attachments/assets/f6f519a2-ff47-47a3-b185-6d98be565122" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="256" height="73" alt="image" src="https://github.com/user-attachments/assets/1d90319e-a8e8-4ef9-a9fb-5ffc23f938d0" />



egrep '(world$)' newfile 
## OUTPUT
<img width="219" height="67" alt="image" src="https://github.com/user-attachments/assets/806c495c-fc09-4fb9-b14c-64c3980b2ffa" />



egrep '(World$)' newfile 
## OUTPUT
<img width="234" height="58" alt="image" src="https://github.com/user-attachments/assets/bf10e336-16ca-44ed-8846-b1567de9cdc6" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="249" height="68" alt="image" src="https://github.com/user-attachments/assets/9311a377-0c56-4fe3-80b4-09454516b838" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="242" height="35" alt="image" src="https://github.com/user-attachments/assets/f652faad-f0fa-455d-bd67-4750911bcf74" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="262" height="33" alt="image" src="https://github.com/user-attachments/assets/c192dec5-d03d-4548-980f-505b4a0c5fca" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="271" height="55" alt="image" src="https://github.com/user-attachments/assets/78a5e857-4b9a-4f63-8da8-4bfcfc354e8f" />


egrep l{2} newfile
## OUTPUT
<img width="234" height="67" alt="image" src="https://github.com/user-attachments/assets/afac4101-bc16-46f1-94fd-6b35ce99ebb8" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="304" height="78" alt="image" src="https://github.com/user-attachments/assets/e04900cd-18d7-4ff1-bf3f-16a2044e24b0" />


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
<img width="226" height="51" alt="image" src="https://github.com/user-attachments/assets/c0f1f4cf-7839-4372-a818-1938f446079b" />



sed -n -e '$p' file23
## OUTPUT
<img width="226" height="51" alt="image" src="https://github.com/user-attachments/assets/ffa990d6-da06-48fb-939a-6722f86ef8dd" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="291" height="170" alt="image" src="https://github.com/user-attachments/assets/a36984a8-9adf-47cc-8f06-17b1990826ae" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="301" height="173" alt="image" src="https://github.com/user-attachments/assets/f25a13de-b0d7-451c-8050-de2b063a371f" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="315" height="179" alt="image" src="https://github.com/user-attachments/assets/2d7209eb-bb52-40e3-a2ae-cc214b8a4daf" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="297" height="119" alt="image" src="https://github.com/user-attachments/assets/3fbcfc18-9f51-46cc-a3d3-b1ead3cf8592" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="304" height="64" alt="image" src="https://github.com/user-attachments/assets/c7d98be3-baad-4e6d-b0e8-6b3813bd09a6" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="291" height="69" alt="image" src="https://github.com/user-attachments/assets/541713a4-ce8e-4d36-9b9c-a1116f321fc1" />



seq 10 
## OUTPUT
<img width="266" height="205" alt="image" src="https://github.com/user-attachments/assets/8c982238-9368-4b51-b54b-d4da44720839" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="279" height="87" alt="image" src="https://github.com/user-attachments/assets/d2d7f331-a2a2-4581-a7dd-6a204cd54a00" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="278" height="84" alt="image" src="https://github.com/user-attachments/assets/3715f664-1240-404a-8fd9-7104f51d84d3" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="291" height="102" alt="image" src="https://github.com/user-attachments/assets/ab945ce4-2a61-4839-b2fd-67e7df59d1b1" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="246" height="86" alt="image" src="https://github.com/user-attachments/assets/04a3f5c0-c7e3-4168-bb7d-3937181567e5" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="267" height="85" alt="image" src="https://github.com/user-attachments/assets/92d50dfd-9025-4b86-890b-ee177e1ef752" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="290" height="91" alt="image" src="https://github.com/user-attachments/assets/ade6d85f-7a5d-4724-be56-fcc892ea0411" />



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
<img width="238" height="114" alt="image" src="https://github.com/user-attachments/assets/fb4a9ed5-2745-43c5-bc1a-2a91797e1bb6" />


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
<img width="245" height="117" alt="image" src="https://github.com/user-attachments/assets/d7231500-fa9c-46a1-8762-782d596c5db5" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="311" height="166" alt="image" src="https://github.com/user-attachments/assets/439c497a-db70-456a-8e1c-bbcfca9552b7" />

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
<img width="314" height="92" alt="image" src="https://github.com/user-attachments/assets/74e9b806-ef1e-4852-91e5-f30757ef71ce" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="328" height="92" alt="image" src="https://github.com/user-attachments/assets/18287010-6315-4b2a-ac4e-cd39ca42e37f" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="230" height="208" alt="image" src="https://github.com/user-attachments/assets/52317186-b200-449d-9bcd-e120a4f44781" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="553" height="203" alt="image" src="https://github.com/user-attachments/assets/85dc9c40-1f9b-4c99-8caa-4594f48e5df7" />


tar -xvf backup.tar
## OUTPUT
<img width="219" height="208" alt="image" src="https://github.com/user-attachments/assets/03740b19-57cf-4f78-a02e-dc4dc618606a" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="125" height="57" alt="image" src="https://github.com/user-attachments/assets/948eec1d-4d42-4aac-87c4-145151737636" />

gunzip backup.tar.gz
## OUTPUT
<img width="123" height="54" alt="image" src="https://github.com/user-attachments/assets/2f36479a-4535-429b-8335-c81f2666276a" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="376" height="110" alt="image" src="https://github.com/user-attachments/assets/73aa51e6-0616-40b9-99fc-f7fbf12e446b" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="260" height="85" alt="image" src="https://github.com/user-attachments/assets/ab895157-6456-444e-a4fe-842d6ff9d675" />


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
<img width="460" height="362" alt="image" src="https://github.com/user-attachments/assets/edd15506-54ab-46fd-8e49-06a027b6b7dd" />

 
ls file1
## OUTPUT
<img width="122" height="56" alt="image" src="https://github.com/user-attachments/assets/7eea329b-930a-451c-afa5-17d4d05d7b49" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
<img width="136" height="55" alt="image" src="https://github.com/user-attachments/assets/03ae06a9-0995-4446-acd0-3dc93b748023" />


 
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
<img width="265" height="192" alt="image" src="https://github.com/user-attachments/assets/cc448bd4-0919-47f8-8c49-a2425ad91f6a" />


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
<img width="470" height="125" alt="image" src="https://github.com/user-attachments/assets/533c1327-746f-41e6-becc-bfe4fac69a3a" />



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
<img width="455" height="106" alt="image" src="https://github.com/user-attachments/assets/5e449e73-c9df-47b3-9bec-77fe6c972233" />

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
## OUTPUT
<img width="448" height="122" alt="image" src="https://github.com/user-attachments/assets/96353d48-890a-4992-8b07-bcae2145e081" />

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
<img width="508" height="85" alt="image" src="https://github.com/user-attachments/assets/5fda44ee-612f-4f96-a492-8eb6743d6e41" />


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
<img width="451" height="89" alt="image" src="https://github.com/user-attachments/assets/f59e10e4-e479-4bc9-8264-fed7a44c546e" />

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
 <img width="319" height="75" alt="image" src="https://github.com/user-attachments/assets/10bc674d-e32e-47ca-9ead-b14a6c5b65db" />

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
<img width="258" height="120" alt="image" src="https://github.com/user-attachments/assets/4fe71d3c-b5b7-4544-af80-6299216ba253" />

 
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
 <img width="254" height="229" alt="image" src="https://github.com/user-attachments/assets/b65eb5b7-7187-44d7-a589-e4667dfeee85" />

 
 
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
<img width="214" height="151" alt="image" src="https://github.com/user-attachments/assets/34a7614b-a445-4c16-acf3-8b9d4925258f" />
 
 
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
 <img width="275" height="106" alt="image" src="https://github.com/user-attachments/assets/b3135e67-61b1-4860-9a75-a00a01ddd5fe" />

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
 <img width="249" height="159" alt="image" src="https://github.com/user-attachments/assets/406ac76d-8e0a-493d-ae1f-3777894c0b02" />

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
<img width="339" height="284" alt="image" src="https://github.com/user-attachments/assets/9e2e7a1d-9534-4dad-9ea6-55df4fe765bd" />


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
<img width="255" height="145" alt="image" src="https://github.com/user-attachments/assets/5977a996-f3b1-4b5e-91f2-e555078df9cf" />

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
<img width="243" height="129" alt="image" src="https://github.com/user-attachments/assets/3bc97d4e-aded-434c-b5a4-4683e97fced3" />

 
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
<img width="283" height="250" alt="image" src="https://github.com/user-attachments/assets/7a4db56f-4861-4d23-bd95-44afc6bf0f1d" />

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
 <img width="389" height="128" alt="image" src="https://github.com/user-attachments/assets/b30ead30-9197-4024-921e-31fea3099cd6" />

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
<img width="338" height="95" alt="image" src="https://github.com/user-attachments/assets/f1a01bcf-0492-4c4d-bbfd-443e9d405b47" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="196" height="106" alt="image" src="https://github.com/user-attachments/assets/d5ebf188-c4e0-4f33-bc60-928cbf418e98" />



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
<img width="229" height="121" alt="image" src="https://github.com/user-attachments/assets/1d4d2128-9613-4068-9711-194d5db83231" />

 
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
 <img width="282" height="139" alt="image" src="https://github.com/user-attachments/assets/95204cd5-da7e-4398-a0af-894cec11e685" />

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
 <img width="240" height="118" alt="image" src="https://github.com/user-attachments/assets/19ebb92e-a811-435c-bbf4-6076b7d69ffb" />

 
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
 <img width="295" height="307" alt="image" src="https://github.com/user-attachments/assets/12122b0b-c314-4aa5-9c77-86922069ba63" />

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
<img width="250" height="103" alt="image" src="https://github.com/user-attachments/assets/9cf88a16-8e8f-4a36-ae71-f4606440b7db" />


# RESULT:
The Commands are executed successfully.
