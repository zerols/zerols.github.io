## move docker's default /var/lib/docker to another directory

```
systemctl stop docker
mkdir /newpath/docker
rsync -aqxP /var/lib/docker/ /newpath/docker
systemctl start docker
docker info
```
