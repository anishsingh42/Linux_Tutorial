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
3. `ls` or `l` - lsit the contents of the current directory in alphabetically order.
      1. *`-l` List in the long way.*
      2. *`-r` Lists in the reverse order.* <br>
 
 Note: At any point if you want more information on any command one can type `--help`. Example: `ls --help`.
 
 ---
 
 ___Adminstritive Privileges in Linux Terminal___
 Use Adminstritive Priviliges to edit sysyem files.
 1. We can use `sudo` (super user do) which gives the current user account root privileges temporarily.
      1. Example : `nano ./file` wont let you edit the `./file` but because you don't have permission but `sudo nano ./file` gives you admistritive privileges to allow you to edit.
2. Instead of writing `sudo` before every command we can also use `su` (switch user) command followed by the account you want to switch to. Instead we are goin to write `sudo su` to switch to the root account(because the root user have 100% access to everything).

---
___Using the package manager (apt-get) to install new applications___

