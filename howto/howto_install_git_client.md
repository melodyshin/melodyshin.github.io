
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

> No file menus show up before your repository has any file.

 * Enable github.io (if U create different url with default one )
```
Source -> Master branch or else -> Save
```

 * Check
```
Browser -> go to https://username.github.io
```
