# How to install git client on centOS 7


## Install
```
$ sudo yum install git
$ git --version
```

* Configure username and email
```
$ git config --global user.name "username"
$ git config --global user.email "your_email"
```

* Check what configured
```
$ git config --list
```
or check Configuration file  ~/.gitconfig

## Create username.github.io

* Create a new repository 

```markdown
GitHub on browser -> Your Profile -> + (New Repository) 
-> name it **"username.github.io"**
```

* Configure repository 
```markdown
GitHub on browser -> Your Profile -> Your Repository
 ->  **Settings** -> GitHub Pages
```

 * Apply theme
```
Select Theme -> create index.html page using default template
-> Commmit
```

   * No file menus show up before your repository has any file.

 * Enable github.io (if U create different url with default one )
```
Source -> Master branch or else -> Save
```

 * Check
```
Browser -> go to https://username.github.io
```

## Add a new file to the repo.

> You can clone remote files anywhere you want

```
$ cd where_you_want_clone
$ git clone the_repository_url_to_clone
  (ex: https://github.com/username/username.github.io )
$ cd your_repo_name_directory
```
 * Make any file or copy files to commit
```
$ make any file
```
> git add -> commit -> push

 * git add
```
$ git add --all
```
 * git commit with a message
```
$ git commit -m "Initial commit"
```
 * git push to master branch
```
$ git push -u origin master
```
