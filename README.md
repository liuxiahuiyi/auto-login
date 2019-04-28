# config in file conf

```
nickname                  ip            user              password                       port(=22)
baoleiji(necessary)   jps.jd.com      wangyike1             ****                           80
sz_client            172.21.51.43     wangyike1
online_machine           ****           admin               ****
```

# usage

## login

The option "generate ssh key pair in machine (y/n)?" would write your ssh pub key to machine you logining, default is "n".

* login baoleiji

```shell
cd ~/auto-login
bin/login
```

* login baoleiji client

```shell
cd ~/auto-login
bin/login sz_client
```

* login online_machine by sz_client

```shell
cd ~/auto-login
bin/login sz_client online_machine
```

## upload/download dir or file

Before you upload/download a dir or file to/from remote machine, you must login that machine with ssh pub key only once. Thereafter you can upload/download a dir or file without login.

* upload local dir $source to sz_client dir $target

```shell
cd ~/auto-login
bin/trans u sz_client $source $target
```

* download sz_client dir $source to local dir $target

```shell
cd ~/auto-login
bin/trans d sz_client $source $target
```

