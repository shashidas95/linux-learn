# Connecting from a Linux Host
Log into the source Linux host
Run the following command in a terminal window
##3 generate a new ssh key pair
 ```bash
  ssh-keygen -t rsa
 ```
Press enter to accept the default location
Optionally, set a password for the key pair
NOTE: If you don't provide a password, anyone with the key and access to the target host can connect using the key. Proceed with caution
Continue with the following command
### output the public key
```bash
  cat ~/.ssh/id_rsa.pub
```
Copy the output ssh-rsa public key to the clipboard
Log into the target Linux machine
Run the following command in a terminal window
### create .ssh directory
```
mkdir ~/.ssh -p
```
### edit the authorized_keys file
```
nano ~/.ssh/authorized_keys
```
Paste the copied public key to the bottom of the file
Press CTRL+O, Enter, CTRL+X to write the changes
Back on the source Linux device, connect to the Linux target using ssh (ie ssh username@hostname)
Type yes and press Enter the first time connecting with a new public key to accept the connection
# Connecting from a Windows Host
Log into the Windows host
Right click the Start menu > Run > Type cmd > Press Enter
Run the following command in the command prompt
### generate a new ssh key pair
```
ssh-keygen -t rsa
```
Press enter to accept the default location
Optionally, set a password for the key pair
NOTE: If you don't provide a password, anyone with the public key and access to the target host can connect using the key
Continue with the following command
### output the public key
```
type %userprofile%\.ssh\id_rsa.pub
```
Copy the output ssh-rsa public key to the clipboard
Log into the target Linux machine
Run the following command in a terminal window
### create .ssh directory
```
mkdir ~/.ssh -p
```
### edit the authorized_keys file
```
nano ~/.ssh/authorized_keys
```
Paste the copied public key to the bottom of the file
Press CTRL+O, Enter, CTRL+X to write the changes
### Back on the Windows device, connect to the Linux target using 
```
ssh (ie ssh username@hostname)
```
Type yes and press Enter the first time connecting with a new public key to accept the connection
