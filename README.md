# cheatsheet
## git
roll back file to particular commit
```
git checkout <hash_commit> -- <file>
```
merge hotfix to master
```
git checkout master
git merge hotfix
```
show config
```
git config --list
```
set local
```
git config --local user.email username@example.com
```
rename local branch
```
git checkout <old_name>
git branch -m <new_name>
```

## Go
creating new mod
```
go mod init <package>
```
## Unix
current time
```
date
```
package reverse dependencies
```
apt-cache rdepends <package>
```
show last lines in file
```
tail -n <count> <filename>
```

## Docker
go into container
```
docker exec -it <container> <shell>
```
go into container as root
```
docker exec -u 0 -it <container> <shell>
```
dump
```
docker run -i --rm postgres pg_dump -h host.docker.internal -U username --password --table tablename dbname  > ~/filename.sql
```
## REGEXP
alternative
```
one|two
```
## Python
set venv
```
virtualenv -p <python_exe> --no-site-packages <dir_env>
```
## Django
drop all migrations
1. delete from django_migrations where app=<app_name>;
2. drop all tables in <app_name>
