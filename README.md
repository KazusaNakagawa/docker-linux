## Linux

linux systemd automation

## Docker environment (M1 Mac)  

### index
- pattern1: docker-compose
- pattern2: build >> run/mount


### pattern1: docker-compose

```dockerfile
$ docker-compose up -d
```

### pattern2: build >> run/mount

1. option (--platform linux/amd64) つけて実行
```docker
$ docker build --platform linux/amd64 -t jupyter_lab:latest .
```

2. mount
```docker
$ docker run -p 8888:8888 -v <host path>:<local path> --name my-lab jupyter_lab
```
