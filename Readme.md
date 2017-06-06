
Docker Commands:
----------------

**Build** container from `Dockerfile` in current directory (and tag it as "friendlyhello")  
`docker build -t friendlyhello .`

**Run** a container by it's tag and map port 4000 to it's port 80  
`docker run -p 4000:80 -i -t friendlyhello /bin/bash`
>NOTE: The terminal will change to the container's terminal

> Starting apache in the container: `service apache2 start`

> ctrl+p then ctrl+q gets you out of that container's terminal

if you've started apache in your container, the server is located at http://locahost:4000  



**List** Running Containers:  
`docker ps`

**Attach** a terminal to a running container:  
`docker attach 9c09acd48a25` where 9c09acd48a25 is the container ID

**Stop** a container by it's ID:  
`docker stop 1fa4ab2cf395`






stop and remove all containers:  
```
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```






    
docker-compose up  

  
List Docker IMages:  
docker images -a  

  
Remove:  
docker rmi Image  
docker rmi -f Image  




Delete ALL images:
  
#!/bin/bash  
# Delete all containers  
docker rm $(docker ps -a -q)  
# Delete all images  
docker rmi $(docker images -q)  






Docker Build IMage from Docker File
docker build -t friendlyhello .

RUn it
