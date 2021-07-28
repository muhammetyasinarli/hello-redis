#How to run redis container? 
	docker pull redis
	docker run --name local-redis -p 6379:6379 -d redis
	docker logs -f local-redis

#Now to validate if the installation is working as expected, we will run 
	redis-cli. 
#For that firstly, I will bash inside the container and run the redis-cli with the following commands.
	docker exec -it local-redis /bin/bash
#This command will get us inside of the docker container for Redis. 
#Once we are inside, we can just fire redis-cli, which will open the command-line interface. 
#Finally, we can send a ping to the CLI, and if everything is working, we will get a PONG response, indicating that the Redis is running properly.
	redis-cli
	ping
	
#In order to check redis store, use below commands
docker exec -it local-redis /bin/bash
get 01
