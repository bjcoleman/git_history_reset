## Git History

This repo is a proof-of-concept regarding git memory of commits when history is re-written.

```
$ git init
$ nano README.md
$ git add README.md 
$ git commit -m "Initial commit."
$ nano login.py
$ git commit -m "Add login credentials."
$ git add login.py 
$ git commit -m "Replace credentials with environment variables."
$ hist = log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short

* 9e9b5f4 2018-01-22 | Replace credentials with environment variables. (HEAD -> master) [Ben Coleman]
* 8413122 2018-01-22 | Add login credentials. [Ben Coleman]
* 8329da5 2018-01-22 | Initial commit. [Ben Coleman]

$ git reset --hard 8329da5
$ nano README.md
$ git add README.md
$ git commit -m "Add command history."
```