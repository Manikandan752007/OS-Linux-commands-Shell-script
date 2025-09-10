<img width="694" height="426" alt="image" src="https://github.com/user-attachments/assets/87dcde27-24d0-4a47-9b65-69fe1f32d845" /># OS-Linux-commands-Shell-scripting
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
<img width="245" height="230" alt="image" src="https://github.com/user-attachments/assets/bf73ac22-ec1c-4561-a9a1-08a7397379df" />



cat < file2
## OUTPUT
<img width="209" height="170" alt="image" src="https://github.com/user-attachments/assets/30c0e508-6f48-4d33-9f9a-114d453a9497" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="367" height="72" alt="image" src="https://github.com/user-attachments/assets/603a2958-0117-45c9-99ce-017efc7c2b6f" />

comm file1 file2
 ## OUTPUT
<img width="313" height="244" alt="image" src="https://github.com/user-attachments/assets/1ae911e9-947b-4cbd-8b66-dfbb296420ab" />

 
diff file1 file2
## OUTPUT
<img width="245" height="343" alt="image" src="https://github.com/user-attachments/assets/d329162f-4058-4b9c-b076-6c135b294dcf" />


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

<img width="243" height="97" alt="image" src="https://github.com/user-attachments/assets/c11ca898-e11f-425c-8e62-54f01ec86893" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="303" height="102" alt="image" src="https://github.com/user-attachments/assets/06a4ca3d-6a8b-4934-b597-c593b289011f" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="364" height="98" alt="image" src="https://github.com/user-attachments/assets/8baf4df8-7dca-433d-a759-6b9dce5ddca2" />


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
<img width="265" height="75" alt="image" src="https://github.com/user-attachments/assets/899456bf-e687-44f2-b111-9ec50447fefc" />



grep hello newfile 
## OUTPUT

<img width="332" height="75" alt="image" src="https://github.com/user-attachments/assets/c9120bb8-74d3-4916-8aab-16c4fb8c0a72" />



grep -v hello newfile 
## OUTPUT

<img width="292" height="82" alt="image" src="https://github.com/user-attachments/assets/25f8d65a-5321-4758-af02-f476ae0afadf" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="372" height="96" alt="image" src="https://github.com/user-attachments/assets/ecc86201-de08-4d51-82bc-c6bdbf55e8c5" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="410" height="73" alt="image" src="https://github.com/user-attachments/assets/e8dcd378-2486-470e-b3c6-3c9d603fbde9" />



grep -R ubuntu /etc
## OUTPUT

<img width="698" height="574" alt="image" src="https://github.com/user-attachments/assets/c597f2d0-8e87-4661-8631-340dc924f971" />


grep -w -n world newfile   
## OUTPUT

<img width="313" height="96" alt="image" src="https://github.com/user-attachments/assets/c1bec975-36fe-4439-86f4-39d2567c12d9" />

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

<img width="371" height="103" alt="image" src="https://github.com/user-attachments/assets/cf3536eb-2da8-4736-a52d-db8943aa6b69" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="383" height="105" alt="image" src="https://github.com/user-attachments/assets/d8960268-9d32-45af-bc5b-95e960ea5bf4" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="391" height="98" alt="image" src="https://github.com/user-attachments/assets/ce59b4ab-6876-43cc-89a4-ae1961da34ad" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="322" height="74" alt="image" src="https://github.com/user-attachments/assets/ced5f6ef-7054-4ae4-a984-c62e6405a507" />


egrep '(world$)' newfile 
## OUTPUT
<img width="320" height="97" alt="image" src="https://github.com/user-attachments/assets/3c76db43-12c6-4329-b2c9-58512cc87418" />



egrep '(World$)' newfile 
## OUTPUT
<img width="302" height="98" alt="image" src="https://github.com/user-attachments/assets/0c261db6-7227-4e35-80ee-0fa7e905f9b2" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="363" height="100" alt="image" src="https://github.com/user-attachments/assets/c133877a-4f78-4497-aebd-a8fa5e319308" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="273" height="74" alt="image" src="https://github.com/user-attachments/assets/e0350f29-f517-410f-acff-5b8a437c8966" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="353" height="78" alt="image" src="https://github.com/user-attachments/assets/dda0c2f9-ff83-4aec-8c77-9f6f97d7674e" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="351" height="72" alt="image" src="https://github.com/user-attachments/assets/771d56b3-7866-4ec7-9691-8ed2d095ebe2" />


egrep l{2} newfile
## OUTPUT

<img width="352" height="76" alt="image" src="https://github.com/user-attachments/assets/a3f1dfeb-cf06-478b-960b-4a5a3d9c666e" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="268" height="96" alt="image" src="https://github.com/user-attachments/assets/60cf6318-a465-4d9d-ba77-b81d751202d2" />


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
<img width="294" height="79" alt="image" src="https://github.com/user-attachments/assets/7c3631e2-3ab9-4951-b0da-e97ef223c5cd" />



sed -n -e '$p' file23
## OUTPUT
<img width="327" height="77" alt="image" src="https://github.com/user-attachments/assets/6873905d-6645-47d1-b672-c3a2898b13d8" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="323" height="225" alt="image" src="https://github.com/user-attachments/assets/69c60fca-d49a-4051-98e5-2579660e4109" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="386" height="224" alt="image" src="https://github.com/user-attachments/assets/77025917-53d6-4078-a8ed-647a59c893d4" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="411" height="227" alt="image" src="https://github.com/user-attachments/assets/4be21808-bfcd-4297-b511-04f991c68926" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="373" height="171" alt="image" src="https://github.com/user-attachments/assets/03baa01c-f49b-4010-bcf0-c2773a796fea" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="338" height="121" alt="image" src="https://github.com/user-attachments/assets/13fc2a46-d55a-4cd3-92ae-0f4c9eca5bba" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="393" height="104" alt="image" src="https://github.com/user-attachments/assets/65c8038d-b83d-40ae-b264-79e2e1c62c84" />



seq 10 
## OUTPUT

<img width="339" height="293" alt="image" src="https://github.com/user-attachments/assets/9398f70c-725e-4a1a-9b53-6834d317f530" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="291" height="126" alt="image" src="https://github.com/user-attachments/assets/ac4534d8-f9f8-41d8-afdf-51840849cfc3" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="305" height="118" alt="image" src="https://github.com/user-attachments/assets/97c96470-ab18-42ba-b70f-5cad79bc2cf2" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="295" height="148" alt="image" src="https://github.com/user-attachments/assets/aa66b7f6-fe85-4ae7-b579-139220f815a4" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="298" height="121" alt="image" src="https://github.com/user-attachments/assets/cdc49189-bc3c-459f-bc4d-4033171fa8fa" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="320" height="129" alt="image" src="https://github.com/user-attachments/assets/6c087abf-742d-47ce-9d4b-8919b020eae2" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="378" height="133" alt="image" src="https://github.com/user-attachments/assets/9f658ca3-0452-4729-956c-4e6aec1adaaa" />

## OUTPUT
sed -n '2,4{s/$/*/;p}' file23
<img width="369" height="126" alt="image" src="https://github.com/user-attachments/assets/0b54a28a-b169-4ffb-8db7-1a859aca0f94" />


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
<img width="318" height="151" alt="image" src="https://github.com/user-attachments/assets/2ed97419-0c93-49c8-a37a-45b84c584c59" />


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

<img width="361" height="150" alt="image" src="https://github.com/user-attachments/assets/03fe82e1-885e-4e1b-9a19-23f6fd930e5d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="424" height="223" alt="image" src="https://github.com/user-attachments/assets/8226e899-c441-4e80-b589-8b9f856d1e24" />

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

<img width="351" height="130" alt="image" src="https://github.com/user-attachments/assets/c31b41fa-b4ae-4658-a200-5b376eb9cbaa" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="479" height="127" alt="image" src="https://github.com/user-attachments/assets/4d37a363-8b91-4a25-8fe3-61b101a2e2b9" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="277" height="451" alt="image" src="https://github.com/user-attachments/assets/991ed264-def5-4448-ae99-6d3bc36f4881" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="713" height="596" alt="image" src="https://github.com/user-attachments/assets/07d17169-0108-436f-9a18-582d7dfe34e2" />


tar -xvf backup.tar
## OUTPUT
<img width="371" height="456" alt="image" src="https://github.com/user-attachments/assets/fdac7813-9281-444f-a58a-9ceadcc1dbb2" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="626" height="241" alt="image" src="https://github.com/user-attachments/assets/62f0d202-4773-4aae-bc42-d13b3e1e713d" />

gunzip backup.tar.gz
## OUTPUT
<img width="369" height="128" alt="image" src="https://github.com/user-attachments/assets/34c4e745-315b-4565-ab12-aa0982dffa44" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="576" height="182" alt="image" src="https://github.com/user-attachments/assets/b7a07c66-7aee-4bad-b5fb-c03182a879b8" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="296" height="130" alt="image" src="https://github.com/user-attachments/assets/6599ed6e-2cef-4699-a08d-f1d2aaf130a3" />


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
<img width="620" height="520" alt="image" src="https://github.com/user-attachments/assets/53091514-9ef2-4497-adf1-4fea48310b68" />

 
ls file1
## OUTPUT
<img width="219" height="88" alt="image" src="https://github.com/user-attachments/assets/7f892a86-8b19-4681-8b50-d66a9453fda9" />

echo $?
## OUTPUT 
<img width="209" height="85" alt="image" src="https://github.com/user-attachments/assets/89e8b850-7fe5-435b-9439-06fe3df13ffe" />

./one
bash: ./one: Permission denied


echo $?
## OUTPUT 
 <img width="248" height="73" alt="image" src="https://github.com/user-attachments/assets/1b4bfe12-caf3-4d3f-b7fe-3d2dfb3c8100" />

abcd
## OUTPUT
 <img width="317" height="80" alt="image" src="https://github.com/user-attachments/assets/362537ae-f7be-47bd-8086-8ef9eb9f06cc" />
 
echo $?
 ## OUTPUT
<img width="268" height="86" alt="image" src="https://github.com/user-attachments/assets/a4c5fe67-594d-4ce4-a594-a46adf2206eb" />


 
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

<img width="364" height="242" alt="image" src="https://github.com/user-attachments/assets/7d37c09d-5aca-4ad9-9899-1dd937b53e22" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="599" height="350" alt="image" src="https://github.com/user-attachments/assets/0461e824-6043-44bd-939b-b7f66fe13b70" />


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
<img width="645" height="345" alt="image" src="https://github.com/user-attachments/assets/f6196667-7e53-4a01-af9b-f45c2f84aa5b" />


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
<img width="522" height="533" alt="image" src="https://github.com/user-attachments/assets/db5cf886-1a52-4d2d-b510-e17360b7b9f8" />



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
<img width="618" height="499" alt="image" src="https://github.com/user-attachments/assets/341562c4-ae86-4591-bf35-f13a3bee7adc" />

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
<img width="467" height="452" alt="image" src="https://github.com/user-attachments/assets/22a5a973-e9b9-4b18-971a-e5adfd7bb5ce" />

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
<img width="545" height="483" alt="image" src="https://github.com/user-attachments/assets/7968e2d6-b7e9-4254-b19b-172a3c9c61a3" />


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
<img width="694" height="426" alt="image" src="https://github.com/user-attachments/assets/2a9dde82-cfd4-45e1-9bda-33d34cf68e56" />


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
## Output:
<img width="631" height="460" alt="image" src="https://github.com/user-attachments/assets/16b4b271-a81e-4e28-9b7b-7744867fe55a" />

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
 
## Output:
<img width="623" height="341" alt="image" src="https://github.com/user-attachments/assets/31ed62a8-12d2-4646-83c8-6c4e15a61d1d" />

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
 ## Output:
 <img width="421" height="461" alt="image" src="https://github.com/user-attachments/assets/debd4427-015a-4e07-a737-b1294aca173e" />

 
 
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
 
 ##Output:
 <img width="665" height="473" alt="image" src="https://github.com/user-attachments/assets/0a78fa74-cd3a-46f2-b252-a26e99c46b3a" />

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

##Output:
<img width="610" height="538" alt="image" src="https://github.com/user-attachments/assets/70cb5da8-e02e-4996-920b-814f615454cc" />

 
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

##Output:
<img width="662" height="487" alt="image" src="https://github.com/user-attachments/assets/32c373cb-03ca-4e60-aa5a-d10ab243ae0b" />

 
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
## Output:
<img width="693" height="458" alt="image" src="https://github.com/user-attachments/assets/5302cb0a-ed99-4153-bd4d-738adaa72891" />

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
<img width="682" height="475" alt="image" src="https://github.com/user-attachments/assets/686a8927-6393-485d-8ada-ada6cec0064e" />


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
<img width="505" height="619" alt="image" src="https://github.com/user-attachments/assets/71c02cb2-675f-46a2-b00a-2715cc5fd9a1" />


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
<img width="298" height="406" alt="image" src="https://github.com/user-attachments/assets/2e2d202e-f9dc-4c84-aa93-2acdf5eeb94a" />

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
<img width="254" height="231" alt="image" src="https://github.com/user-attachments/assets/c0f710c8-f5bc-4505-8147-4bd27525b232" />

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
<img width="311" height="414" alt="image" src="https://github.com/user-attachments/assets/15d21a18-2bad-4ecf-a17b-5593b1c10f15" />

 
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
<img width="712" height="486" alt="image" src="https://github.com/user-attachments/assets/b98a58aa-f0c6-4a70-a931-cec5dcd6de39" />

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
 <img width="714" height="526" alt="image" src="https://github.com/user-attachments/assets/63efe0f4-a3b6-44ff-a8c9-30e7235508ca" />

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
<img width="490" height="308" alt="image" src="https://github.com/user-attachments/assets/35719de5-602a-4bb3-972d-72f7a31f7826" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="462" height="153" alt="image" src="https://github.com/user-attachments/assets/27e2b33a-37fd-40bc-bdc4-6e60b137e95c" />


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
<img width="275" height="531" alt="image" src="https://github.com/user-attachments/assets/cead9d8c-a2e7-413d-b8b7-d0fe1e046d0f" />

 
 
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
<img width="316" height="401" alt="image" src="https://github.com/user-attachments/assets/883e1a59-4b0f-4ee3-8aaa-ce5efd271fda" />

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
<img width="345" height="452" alt="image" src="https://github.com/user-attachments/assets/46e8f6cc-33c9-4e7c-8fc4-0cccc115467e" />

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
<img width="280" height="456" alt="image" src="https://github.com/user-attachments/assets/891b0793-0e66-4110-b31d-fcb5d24e5769" />

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
 <img width="641" height="385" alt="image" src="https://github.com/user-attachments/assets/00f3d23f-8313-40a3-a44a-4d83ab2a2a5b" />

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
<img width="670" height="308" alt="image" src="https://github.com/user-attachments/assets/56b9df88-364c-4f12-b0b1-bf5e401a05c6" />


# RESULT:
The Commands are executed successfully.
