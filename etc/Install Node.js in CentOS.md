# Install Node.js in CentOS
Download Node.js Linux Binaries (x86/x64) from [here](https://nodejs.org/en/download/). I use `wget` to download it.
```bash
wget https://nodejs.org/dist/v8.11.3/node-v8.11.3-linux-x86.tar.xz
```
Use `xz` command to uncompress the file "node-v8.11.3-linux-x86.tar.xz"
```bash
xz -d node-v8.11.3-linux-x86.tar.xz
```
Then you get the file `node-v8.11.3-linux-x86.tar`. Use `tar` command to extract the file.
```bash
tar -xvf node-v8.11.3-linux-x86.tar
```
Then you will get the directory "node-v8.11.3-linux-x86"

Edit the `/etc/profile` add following content before "export PATH USER LOGNAME MAIL HOSTNAME HISTSIZE HISTCONTROL" this line.

```
#set for nodejs
export NODE_HOME=<YOUR_NODE_DIRECTORY>
export PATH=$NODE_HOME/bin:$PATH
```

use following command to enable the config.
```bash
source /etc/profile
```

type `node -v` or `npm -v` to verify that it is installed correctly or not.
```bash
[root@localhost ~]# node -v
v8.11.3
[root@localhost ~]# npm -v
5.6.0
```

EOF