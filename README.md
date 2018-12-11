# Create docker image using Dockerfile- Apache-2.4 and PHP-7.2
Docker is the most revolutionized technology in virtualization world nowadays. Docker is actually an open source project which provides container technology. A container is a lightweight VM(virtual machine) or a process which allows us to install Linux based applications inside it. The container doesn’t have its own Kernel, RAM, CPU and Disk but it uses the underlying OS kernel, RAM, CPU cores and Disk.

**Step 1- Install Docker in Ubuntu 16.04:**

Please follow Step by Step installation of Docker Ubuntu 16.04 in my previous blog- 
```
https://linuxhowtoguide.blogspot.com/2018/08/how-to-install-docker-in-ubuntu-1604-lts.html
```

**Step 2-  download Dockerfile:**

run following command on you ubuntu terminal
```
git clone https://github.com/amarsingh3d/dockerfile_apache-2.4_php-7.2.git

```

**Step 3- Build own Docker Image:**
```
docker build -t ubuntu16:apache-php7.2 .
```

**Step 4- Test our docker image by running a Container:**
```
docker run -dit --name webS -p 8080:80 ubuntu16:apache-php7.2
```
**Verify Running Container**
```
docker container ls
CONTAINER ID        IMAGE                                   COMMAND                  CREATED             STATUS              PORTS                        NAMES
0cc9465284a9        ubuntu16:apache-php7.2                "/bin/sh -c '/usr/sb…"    14 seconds ago      Up 11 seconds    0.0.0.0:8080->80/tcp              webS
```

**Step 5- Verify container and PHP version**
In order to Verify container and PHP version open browser and access host IP address with port 8080-
```
 http://hostip:8080
```



