# Jenkins CI/CD pipeline for IAC


1. Initialize docker swarm

```
% docker swarm init
```

2. Create secrets

```
% echo admin | docker secret create jenkins-user -
% echo admin | docker secret create jenkins-pass -
% docker secret ls
```

3. Deploy the stack

```
docker stack deploy -c jenkins-stack.yml jenkins
docker stack ls
docker service ls
```