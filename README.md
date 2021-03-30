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
Редактирование коммита в середине

1.
```
git rebase --interactive HEAD~4
```
2. Видим
```
pick ac91b6d first commit
pick 3feff7d second commit
pick f4cbf30 third commit
pick c0271e5 fourth commit
```
первая строчка относится в самому раннему коммиту, последняя - к самому позднему. Нужно заменить pick на e в первой строчке и выйти из редактора. После этого можно отредактировать нужные файлы и сделать
```
git add <changed files>
git commit --amend
git rebase --continue
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
sigterm
```
kill -15 [pid]
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
restore
```
docker exec -i container_DB psql -v ON_ERROR_STOP=1 -U username --password dbname < ~/filename.sql
```
copy
```
docker cp filename mycontainer:filenameDest
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

## Postgres
database size
```
SELECT pg_size_pretty(pg_database_size('dbname'));
```

any
```
ANY('{FOO,bar,%oo%}')
```
