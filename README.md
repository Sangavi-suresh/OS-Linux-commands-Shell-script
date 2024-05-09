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
![305638280-75a5512e-1a3b-45f7-ad9a-369f872d4e8a](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/13adca41-7aa2-472d-8d37-fa54a60c11b0)

comm file1 file2
 ## OUTPUT
 
![305638353-06aaf5ba-ea64-4e0c-8499-115f566e830f](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/9ffd72d2-321f-4445-a81f-4ac1a10b49e8)

 
diff file1 file2
## OUTPUT

![305638538-dd5d576c-fdad-4142-8a42-957143d516bb](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/e9c13317-8e8d-44a8-b014-53c5c50ecaf0)


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

![305638593-057abf47-bdbc-4ed1-b8c0-df0302401aad](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/75c2aea7-9ee5-4bdc-8260-2e15c867cb98)



cut -d "|" -f 1 file22
## OUTPUT

![305638603-64f3b346-85d6-40e6-a5ca-0795b38c67c2](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/96d75dee-a07d-4c86-945f-d09b21bc6846)


cut -d "|" -f 2 file22
## OUTPUT

![305638740-26e24d41-1567-4bb7-a427-463ae5f32f95](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/4b30f2d4-70b0-4c7b-bd68-20a225217c54)


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

![305638765-a75c35a9-3407-45bb-a60c-51ac39e93dd0](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/262fed21-a787-4fa2-be62-e428b9019f97)


grep hello newfile 
## OUTPUT

![305638777-1fed07d9-9937-4958-934c-dae3f0c403d3](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/6a18e7e9-dd29-4d7c-82b2-6b00efcdabb7)



grep -v hello newfile 
## OUTPUT

![305638788-675e0427-572c-4aca-953c-cc45455944ae](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/9bb9e4fa-f899-4ef9-86b4-f1f027c87588)


cat newfile | grep -i "hello"
## OUTPUT

![305638803-8dea6fe3-2ada-4ab9-ae14-db1f7eaa36f7](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/886ea13c-1e62-4ca6-9003-b72248079f0c)



cat newfile | grep -i -c "hello"
## OUTPUT

![305638905-fd4ce646-de28-4957-83b6-e305c1f4439a](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/61eaa109-27db-4d22-b2e0-fccba3b9d667)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

![305638979-dfaf1853-3e52-470b-9bc5-38d3057ce4b2](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/2b9080e2-40f3-4f34-8879-5166e3103700)

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

![305638995-63f44836-f6b6-4d66-bdf4-9a53fb6fe0d4](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/323aa969-b8f5-463d-bfc9-88421f2c43ad)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![305639002-8cc574fc-24a7-4e1d-bfd0-56ca0ff8dd45](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/ec955196-987c-47a6-b865-d1f80a610e58)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![305639007-50e2bb9b-2c9b-4df4-9d46-903adbd0e6da](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/90ec667d-7718-4457-add2-e611e0196fcb)



egrep '(^hello)' newfile 
## OUTPUT

![305639010-67ad9538-9b91-423e-8266-1fb2edbc9d40](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/8c588581-96fa-4172-8272-1a0a0a9296c9)


egrep '(world$)' newfile 
## OUTPUT

![305639010-67ad9538-9b91-423e-8266-1fb2edbc9d40](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/20efd49d-db91-4209-a94f-6e7788f24bf2)


egrep '(World$)' newfile 
## OUTPUT

![305639035-fb6711f3-9556-4718-a749-555f06debab1](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/14c769f4-1eff-4ef9-bbe6-6f0884ac363c)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![305639048-cc9d61d6-82b4-42a2-a3eb-593038c19fc7](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/52368228-57ab-4c76-927c-9f6507873fec)


egrep '[1-9]' newfile 
## OUTPUT

![305639050-6d099778-2b88-4e6f-8b06-c40b2f09a638](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/9190d3ec-6237-4ffb-bacf-a3ec1ba61195)


egrep 'Linux.*world' newfile 
## OUTPUT

![305639093-d1c365df-03a4-4e54-928e-4a381e058096](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/7f8dfb87-8e30-4a45-b00a-90a610a83868)

egrep 'Linux.*World' newfile 
## OUTPUT

![305639103-591ab9e6-e543-40a3-a4ec-f9012f8ceadf](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/a62cf6f7-d5ec-4128-bdbb-f0c35b64fe08)

egrep l{2} newfile
## OUTPUT

![305639113-98619322-54a4-4a4c-ad34-fa84af7dfff4](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/21c1de33-f439-447b-a355-d65daf35dd04)


egrep 's{1,2}' newfile
## OUTPUT 

![305639119-91245c5a-f669-4b1c-8641-44667f0689f7](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/8b81c302-ea28-44a0-af53-0590e42a136f)

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

![305639126-6067006c-52ab-4263-bb7c-8675a5cba9d7](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/743f3865-b86c-41f8-b0bb-02c38c01e749)


sed -n -e '$p' file23
## OUTPUT

![305639157-ea154aa6-2031-4bc9-a5fa-d246da2078ce](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/806e0272-59ee-4623-a297-c159b352181f)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![305639157-ea154aa6-2031-4bc9-a5fa-d246da2078ce](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/331147f9-f1eb-4a6c-842f-b096d64a693e)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![305639166-b35d81b6-ed9b-4d25-b8cb-d3ca5c25fdf0](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/15081827-683d-424e-bd4c-f8d8f8d2761c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![305639177-e6e1ba26-5291-43fd-8f40-d6fe00a20498](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/7460a4dc-7381-4801-8370-256536006f45)


sed -n -e '1,5p' file23
## OUTPUT

![305639187-d727de65-8c1f-474b-a1a7-2d87bbc4b354](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/f2d91263-28e7-4290-9b46-f4cfc710db4f)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![305639194-ca6da655-591e-498b-9afb-e9bcd8e09c64](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/9c8c2fc8-8ac2-450b-a48f-9ef5bdc09970)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![305639202-7a82bd4e-4d0e-4340-89d1-882aa938ae94](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/216f75b9-df8d-438b-ac94-18c3b308ea8f)


seq 10 
## OUTPUT

![305639219-fa19b57d-1c9d-4bef-81a8-159ef1e802be](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/b6d4be8c-470b-41d4-a29a-b58980f2df37)


seq 10 | sed -n '4,6p'
## OUTPUT

![305639234-a4650fd0-7816-4e90-88fe-036a692d2e76](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/e7191b79-9f37-4759-b782-2afb02e85dd2)


seq 10 | sed -n '2,~4p'
## OUTPUT

![305639247-e76d46db-4e87-4616-adf3-209f22705a28](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/3631eee1-e341-4494-8d1d-07ab0c55010d)


seq 3 | sed '2a hello'
## OUTPUT

![305639257-b251a39b-a769-44e6-aca2-a4a33e8afc48](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/9fd6e939-1bf0-4c4e-b082-f3fa3fc48090)


seq 2 | sed '2i hello'
## OUTPUT

![305639257-b251a39b-a769-44e6-aca2-a4a33e8afc48](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/db26a346-5923-4348-accd-1b57fb11ab5a)

seq 10 | sed '2,9c hello'
## OUTPUT
![305639305-02460176-5dbc-4cd3-86e2-676ef79130bc](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/69255b1f-e79d-470e-b8b3-1375fefc4f17)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![305639312-757e595f-068c-4a2d-9a74-a0c5c280d674](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/21d56aa5-b0a1-47ce-a835-c321b758319f)


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
![305639387-9dcd56c0-8260-4a34-a658-4a9bedfc00a6](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/177b088e-37fd-4005-8c00-d562d4878aa9)


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

![305639402-10564297-a8ca-42e7-9e7b-11d2f5823b34](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/f79321bf-49a8-4f56-b311-2b593677dab8)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![305639440-9ddada14-d8d3-4b5a-a383-4e756bac6c9c](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/cc734b90-8749-47ef-95a4-197ba5f0da0c)

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

![305639452-a3958730-a84b-4be3-934c-75127fd45e20](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/36158a3d-05e8-459f-baf5-88b38aa38a57)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![305639476-36ba05c2-828f-4cf0-b89c-7704eb2a9ca0](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/be57b021-4ed1-4269-a2ad-9114da7f6a02)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![305639489-59aebb74-5bab-4b16-856c-0702c0987aa0](https://github.com/Sangavi-suresh/OS-Linux-commands-Shell-script/assets/118541861/b580b584-3ed0-46bc-9f6c-ea714f94a3c7)

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
```
Enter the number
5
Number is palindrome
```
# RESULT:
The Commands are executed successfully.
