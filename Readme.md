## CREATE A TORRC.DEFAULT
File: /torrc.default

## BUILD THE DOCKER IMAGE
Run the following command to build the docker image.

```bash
docker build -t simeononsecurity/docker-tor-relay-middle:latest .
```

 
## RUN THE DOCKER CONTAINER
```docker
docker run -d \
--restart always \
-p 9001:9001 \
--name torrelay \
simeononsecurity/docker-tor-relay-middle:latest
``` 

## TEST
Get your current ip

```curl -L http://ifconfig.me```

Get your ip through the tor socks proxy

```curl --socks5 http://localhost:9050 -L http://ifconfig.me```

<a href="https://simeononsecurity.ch" target="_blank" rel="noopener noreferrer">
  <h2>Explore the World of Cybersecurity</h2>
</a>
<a href="https://simeononsecurity.ch" target="_blank" rel="noopener noreferrer">
  <img src="https://simeononsecurity.ch/img/banner.png" alt="SimeonOnSecurity Logo" width="300" height="300">
</a>

### Links:
- #### [github.com/simeononsecurity](https://github.com/simeononsecurity)
- #### [simeononsecurity.ch](https://simeononsecurity.ch)
