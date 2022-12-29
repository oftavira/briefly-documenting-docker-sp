
# *Briefly-documenting-dockers*

### By [Om Tav at appme](https://appme-servicios.web.app)

![Cover image](cover.png)

<br>

Hello 'world'

<br>

***

<br>

## 1 -. What is docker and how can it help us to deploy better apps?

<br>

Docker is a tool designed to make it easier to create, deploy and run applications by
creating containers, a container is a lightweight, standalone and executable package
that includes everything that an application needs to run (even a complete operative system OS)
In fact, creaating a docker container is like creating a virtual machine that can run everywhere.

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

If you are in a linux machine we can install docker with snap.

```
    $ sudo apt update
    $ sudo apt install snapd
    $ sudo snap install docker
```

For windows or mac, the recomendation is to search the instructions with a chat GPT engine, 
or to ask our team at [appme](https://appme-servicios.web.app) and we will be happy to 
help you :D.

<br>

## 3 -. How to run a container?
To run a container we need to use the command docker run, this command will download
the image of the container that we want to run and then it will run it, we can specify
the version of the image that we want to run.

<br>

## 4 -. Creating shortcuts with custom scripts

Another tool that can be used to perform task in a more efficient way is to write python scripts and execute
this tools from sh. This can be done with echo, python, and with a pipe standard.
