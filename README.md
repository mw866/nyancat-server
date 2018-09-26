# Nyancat Telnet Server

Docker Image for a nyancat telnet server with onenetd.


## Demo

```bash
$ telnet [IP address or hostname]
```


## Usage

### Telnet Server
```bash
$ docker run -d --name nyancat-server --restart=always -p 23:23 mw866/nyancat-server
```

##### To view:
```bash
$ telnet <localhost or serverhost>
```



## Dependencies

### [klange/nyancat](https://github.com/klange/nyancat)
Checkout 「[Nyan Cat Telnet Server](http://nyancat.dakko.us/)」 project homepage for demos.

### [offog.org/code/onenetd/](http://offog.org/git/onenetd)
> By default, 40 connections are allowed at once.

View `onenetd` help document by running `$ docker exec nyancat-server sh -c "onenetd -h"`


## Build
```bash
docker build -t nyancat-server . 
```

### Test locally
```bash
$ docker run -d  -p 23:23 --name nyancat-local nyancat-server
$ telnet localhost
$ docker kill [container_id]
```

## Author
[**Chris Wang**](https://chriswang.tech)  
Based on [**Wei He**](https://whe.me) 