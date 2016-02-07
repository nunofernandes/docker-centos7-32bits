centos-7-32bits Docker Image
===============

This dockerfile creates a centos 7 32 bits image.

--

1) Create the image

```bash
git clone https://github.com/nunofernandes/docker-centos7-32bits-scratch
cd docker-centos7-32bits-scratch
		docker build -t centos7-32-build .
		docker run -it --privileged -t centos7-32-run centos7-32-build
		docker cp centos7-32-run:/tmp/centos7*bz2 .
cd ..
```

2) Create a usable centos 7 32 bits image

```bash
git clone https://github.com/nunofernandes/docker-centos7-32bits
cd docker-centos7-32bits
	mv ../centos7*bz2 .
	docker build -t centos7-32 .
cd ..
```

3) Run the image
```bash
$ docker run -ti centos7-32 /bin/bash
[root@6d0a00ff6362 /]# uname -a
Linux 6d0a00ff6362 4.3.4-300.fc23.x86_64 #1 SMP Mon Jan 25 13:39:23 UTC 2016 i686 i686 i386 GNU/Linux
[root@6d0a00ff6362 /]# cat /etc/redhat-release 
CentOS Linux release 7.2.1511 (AltArch) 
[root@6d0a00ff6362 /]# rpm -qf /bin/bash
bash-4.2.46-19.el7.i686
```

License
-------

This code is licensed under the GPLv2.
