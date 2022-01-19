# Linux Tutorial
---
___Learning Linux Essentials___

1. `pwd` - printing working directory.
2. `cd` - change the working directory. 
      1. *`/` Forward slash represents the root directory or siginifies the absolute path.*
      2. *By not writing forward slash it represents relative path.*
      3. *`./` Period forward slash represents current directory.*
      4. *`~` Tilt symbol takes you back to the home directory.*
      5. *`../` Siginifies the parent directory.*
3. `ls` or `l` - list the contents of the current directory in alphabetically order.
      1. *`-l` List in the long way.*
      2. *`-r` Lists in the reverse order.* <br>
4. `nano` - to make a file.
5. `mkdir` - make a directory.
6. `cat` 
 
 Note: At any point if you want more information on any command one can type `--help`. Example: `ls --help`.
 
 ---
 
 ___Adminstritive Privileges in Linux Terminal___
 Use Adminstritive Priviliges to edit sysyem files.
 1. We can use `sudo` (super user do) which gives the current user account root privileges temporarily.
      1. Example : `nano ./file` wont let you edit the `./file` but because you don't have permission but `sudo nano ./file` gives you admistritive privileges to allow you to edit.
2. Instead of writing `sudo` before every command we can also use `su` (switch user) command followed by the account you want to switch to. Instead we are goin to write `sudo su` to switch to the root account(because the root user have 100% access to everything).

---
___Using the package manager (apt-get) to install new applications___

You might not have permissions to install remove or perform other actions on the current account, thats where `sudo` come in role to give you access of root account.
1. __Install__ :  `sudo apt-get install <name_of_application>`. Eg: `sudo apt-get install bluefish`
      1. Note: When you install something it connects to Ubuntu Repository. There might be packages of appilications not being a part of Ubuntu Repository, for that we have a different command.
      2. __Install packages not in ubuntu Repository__ : `sudo dpkg -i <file_path>`. Eg: `sudo dpkg -i ./ google-chrome-stable_cuurent_amd64.deb`. `dpkg` allows you to download `.deb` files.      
2. __Remove__ :  `sudo apt-get remove <name_of_application>`. Eg : `sudo apt-get remove bluefish`
3.  __Keeping programs updated in Linux__ : `sudo apt-get upgrade`.
4. __Searching through the repositories to find new apps__ : Search the Ubuntu Repository with `apt-cache search bluefish`. Will return files with term _bluefish_ with it.
5. __To check whether e have something installed__ : `apt-cache policy <name_of_application>` . Eg : `apt-cache policy gimp'.

---
___File permissions and ownership explained___

1. __Change the OwnerShip of the file__ : 
      1. __Single File__: `sudo chown user:group <file_name>`, Eg: `sudo chown root:Anish_Singh files.txt`.
      2. __Directory__ : `sudo chown user:group <directory_path_name>` , Eg: `sudo chown Anish_Singh:Anish_Singh ./mydirc`. The above line of code will change the ownership of the directory but not the files in it. Inorder to change the ownership of the files inside the directory perform the recussive action by writing `sudo chown -R Anish_Singh:Anish_Singh ./mydirc`.
3.  __Change the Permission of the file__ : `sudo chmod <premission_sequence> <file_name>`.
      1. *`6` represents `-rw`*
      2. *`4` represent `r`.*
      3. *`2` represents `w`*
      4. *`1` represents `x`*
      5.  *`7` represents `-rwx`.*
      
      Eg: `sudo chmod 664 files.txt`.<br>
      <br>The above statement 664 will give -rw permission to user and group and only read permission to others.
      To give two or more permission to a file add the tow permission. Eg: for -rw add r+w which will be 4+2=6.<br>
      <br>Eg: `sudo chmod g-r files.txt`.<br>
      The above statement g-r removes the read permission from the group.

3.__To remove a singular files__ : `rm <file_name>`. Eg: `rm files.txt`.











