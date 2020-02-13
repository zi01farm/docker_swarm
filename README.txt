Docker Swarm Commands

# create a swarm in manager node
docker swarm init --advertise-addr <MANAGER-IP>
# this should make a join token, save this token!
'docker swarm join-token worker' to show the join token again

# check state of Swarm
docker info

# view info about nodes
docker node ls

#in worker: to join node to swarm as worker
docker swarm join \ <TOKEN>

# deploy a service (helloworld in this case) in the swarm from manager
docker service create --replicas 1 --name helloworld alpine ping docker.com

# see list of running services
docker service ls

# scale a service to a number of instances across machines
docker service scale <SERVICE-ID>=<NUMBER-OF-TASKS>

# remove a service
docker service rm <SERVICE-ID>
