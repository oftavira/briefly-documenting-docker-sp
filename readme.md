
# *Briefly-documenting-dockers*

<br>

Hello 'world'

<br>

***

<br>

## 1 -. What is docker and how can it help us to deploy better apps?

<br>

Docker is a tool which aims to make it easier to create, deploy and run applications by
creating containers, a container is a lightweight, standalone and executable package
that includes everything that an application needs to run.In fact, creaating a docker container
is like creating a virtual machine that can run everywhere.

A real world app is built with many different components, for example, a web app can be
composed of a web server, a database, an in-memory cache, and so on. Each of these components
can run in its own container, where each container provides the necesary functions to provide
a specific service.

Containers are more lightweight and more portable than virtual machines.
Once we have our app in a container we can deploy it in any machine that has docker installed
and containers also can be nested, so we can have a container inside another container, this
is very useful when we want to deploy our app in a cloud provider and we want to scale its
cappabilities due to a high demand of users, or small it down when needed.


<br>

## 2 -. How to install docker?

<br>

In linux we can install docker with snap.

```
    $ sudo apt update
    $ sudo apt install snapd
    $ sudo snap install docker
```


<br>

## 3 -. How to run a container?

Basics: Starting the service

```
    $ sudo systemctl start docker
    $ sudo su
```
In the following command replace the term with an image like alpine or debian
to see the available images
```
    $ docker search <TERM2SEARCH> 
```

To pick an image, for example one that offers the capacities to act as a dedicated
web server, we would like to try nginx
```
    $ docker pull nginx
    $ docker run -d --name firstnginx -p 80:80 nginx
```

If we want to attach the container to the current terminal

```
    $ docker run -d --name acutewebsite -p 80:80 nginx
    $ docker attach acutewebsite
```
In a more general way, we can execute commands in the container
```
    $ docker run -d --name hackthisserver -p 80:80 nginx
    $ docker exec -it hackthisserver /bin/bash
```

