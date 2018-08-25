

1. build

```
docker build -t win7/webdav .
```

2. run

```
docker run -it --rm -p 8080:8080  -v `pwd`:/etc/webdav win7/webdav
```