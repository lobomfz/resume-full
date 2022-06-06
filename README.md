TODO:
- Rate limit message
- Clear console on success
- Prettier console
- Mobile-only stuff
- Better jenkins/docker deployment?
- Adjust for load balancing & Least load
- K8S AWS Auto deploy
- Add psql on node
- Age?
- Github webhook on jenkins
- Code cleanup
- Git cleanup

How to set-up dev environment:

git clone --recurse-submodules https://github.com/lobomfz/resume-full/ && cd resume-full

docker-compose up

access http://localhost/jenkins and get key by using the following command:

docker exec -it resume-full-jenkins-1 cat /var/jenkins_home/secrets/initialAdminPassword

create a jenkins user and get an api key on http://localhost/jenkins/me/configure

create a pipeline job, default name is "Self Building Resume Pipeline"


edit .env accordingly

mv .env_template .env

re-run compose (Control+c, then docker-compose up)
