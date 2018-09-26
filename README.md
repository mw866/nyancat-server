# Nyancat Telnet Server

Docker Image for a [nyancat](https://en.wikipedia.org/wiki/Nyan_Cat) telnet server with onenetd.

![nyancat](https://upload.wikimedia.org/wikipedia/en/e/ed/Nyan_cat_250px_frame.PNG)


## Demo

```bash
$ telnet nyancat.chriswang.tech
```

## Use

### Start Server
```bash
$ docker run -d --name nyancat-server --restart=always -p 23:23man
```

### View on Client
```bash
$ telnet <IP address|serverhost>
```

### Quit on Client

```
telnet> ^]
telnet> quit
```

## Develop

### Build

```bash
docker build -t nyancat-server .
```

### Test

```bash
$ docker run -d  -p 23:23 --name nyancat-local nyancat-server
$ telnet localhost
$ docker kill [container_id]
```

## Dependencies

### [klange/nyancat](https://github.com/klange/nyancat)
Checkout [**Nyan Cat Telnet Server**](http://nyancat.dakko.us/) project homepage for demos.

### [offog.org/code/onenetd/](http://offog.org/git/onenetd)
> By default, 40 connections are allowed at once.

View `onenetd` help document by running `$ docker exec nyancat-server sh -c "onenetd -h"`

## Acknowldgement 
Based on [**wei/nyancat-server**](https://github.com/wei/nyancat-server) by [**Wei He**](https://whe.me) 