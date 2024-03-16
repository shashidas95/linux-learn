# linux-learn
- install essential tools
``` sudo apt install -y build-essential linux-headers-$(uname -r)```
# if ssh: connect to host localhost port 22: Connection refused
-  Remove SSH with the following command:

``` sudo apt-get remove openssh-client openssh-server ```
- Install SSH again with:

``` sudo apt-get install openssh-client openssh-server ```
It will solve your problem.

-  To find active user 
``` w ```
-  briefly show the ip address
``` ip --brief addr show ```
- in linux terminal paste option is
  ``` ctrl + shift v ```
- sudo -i will give you a root shell.
