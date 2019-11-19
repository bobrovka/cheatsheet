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
copy to clipboard
```
cat filename.txt | clip
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

