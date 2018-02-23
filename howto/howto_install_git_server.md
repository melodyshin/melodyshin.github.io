
# How to install git server on centOS 7

Assuming you already installed git.

## Assign a user only for your git server
```
$ adduser git
$ passwd git
$ su git
```

## Generate RSA key pair

```
$ cd ~  (move to home directory)
$ ssh-keygen -t rsa
  Generating public/private rsa key pair.
  Enter file in which to save the key (/home/git/.ssh/id_rsa) --> enter
  Enter passphrase (empty for no passphrase ): --> enter
  Enter same passphrase again : --> enter
```
Check the keys
```
ls -al ~/.ssh --> check id_rsa,id_rsa.pub,authorized_keys
```

> If any git client want to connect this git server without prompting any password
>  then do the same thing on the client's node
>  and add client's public key(id_rsa.pub) at the end of server's "authorized_keys" file

```
Server's authorized_keys

ssh-rsa BLA_BLA_KEY1 client1@domain1
ssh-rsa BLA_BLA_KEY2 client2@domain2
```

## Create Directory for Repository
> repository_name should ends with ".git"
> ex) project.git
```
$ mkdir repository_directory/repository_name
```

## Change Owner
```
chown -R git:git repository_directory/repository_name
su git
```

## Initialize Repository
```
$ cd repository_directory/repository_name
$ git --bare --shared init
  !Initialized empty Git repository in repository_directory/repository_name
```

## Create link ( optional )
```
$ cd --> to git's home directory
$ ln -s repository_directory/repository_name
```

 * Check from client
```
$ git clone git@server_domain:repository_name

if you don't create any link, you have to try
$ git clone git@server_domain:repository_directory/repository_name
```

## For Security
Change login shell of git

 * Before
```
git:x:1001:1001::/home/git:/bin/bash
```

 * After
```
git:x:1001:1001::/home/git:/usr/bin/git-shell
```
