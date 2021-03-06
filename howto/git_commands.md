# Git Commands

### Clone

> You can clone remote files anywhere you want

```
$ cd where_you_want_clone
$ git clone the_repository_url_to_clone
$ cd your_repo_name_directory
```
> Two types of URL are possible
> 1) http
     ex) https://github.com/username/repository_name
>
> 2) ssh
>    ex) git_id@server_domain:repository_path

### Add a new file to the repo.
> git add -> commit -> push

 * git add
```
$ git add --all
```
or
```
$ git add file_to_add
```

 * git commit with a message
```
$ git commit -m "Initial commit"
```

 * git push to master branch
```
$ git push -u origin master
```

### Check status
```
$ git status
```

### Force to **overwrite** a local file from local repository (to recover)
```
$ git checkout -- file_path/file_name
```

### Force to **overwrite all files** from remote
```
$ git pull remote
ex) git pull origin
```

