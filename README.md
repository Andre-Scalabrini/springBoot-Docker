# springBoot-Docker
springboot docker image to class on day 16/04/2024

To build the docker image:

```docker build -t spring-boot-docker:spring-docker .```

Verify the image:

```docker image ls```
If the image was created, it should appear as 
**REPOSITORY           TAG**
**spring-boot-docker   spring-docker**

To run the image on a container:
```docker run -d -p 8080:8080 spring-boot-docker:spring-docker .```

And, to check if the API is working, simply run:
```curl -v localhost:8080/api/hello```

If this works, it should appear like this on the terminal:
```
Trying 127.0.0.1:8080...
* Connected to localhost (127.0.0.1) port 8080 (#0)
> GET /api/hello HTTP/1.1
> Host: localhost:8080
> User-Agent: curl/7.81.0
> Accept: */*
>
* Mark bundle as not supporting multiuse
< HTTP/1.1 200
< Content-Type: text/plain;charset=UTF-8
< Content-Length: 29
< Date: Wed, 17 Apr 2024 00:36:38 GMT
<
* Connection #0 to host localhost left intact
Hello spring boot application
```
