#  Frontend web application which is contains html,css and js source code.
I am using #Git,#Maven,#Docker and #K8s tool for this application.

GIT:
---
First I am clon the code form my dedicated github repository .

MAVEN:
----
then I build source code which is clone from dedicated repository using maven whixh is build management tool. it will be first read pom.xml configuration file  after that it will build the code.
it will generate artifactory code in war/jar deployment file in default created directory named is target.
the target directory also contains test report.

DOCKER:
------
after build source code we create Image using docker.
docker is opern source platform that allows you to build,test and deploy application quickly.
container is standard unit of docker,
we deploy our deployment file in container with required libraries and dependensies to run application.
we install web server or application server based on source code of application.
if all required configuration completed so  we create container using docker commit command.
But there is another way we create docker image using Dockerfile.
Dockerfile is set of instruction in linux command and some components such as FROM,RUN,ADD,EXPOSE.
 When we run "docker build" command on current directory the dockerfile and all server paths must be the current directory to build the image.
it will automatically install software and copy deployment file into dedicated server in web deployment directory.
then we push our created image to dockerhub using the "docker push" command.

K8S:
---
Now, we are deploying application  which is we created image and push to my docker registry.
In Docker world we create containers but in Kubernetes world we create pods which are small deployable units of Kubernetes.
we are useing kubernetes object such as Deployment and service which is we defined in manifest yaml file.
We are using Kubernetes objects like deployment and service which we define in the manifest yml file.
after creating deployment and service yaml file we can deploy our application on any cloud server.
we can access our application from container inside the pod using service object which is enable communation between pod and conatiner.
and we access from browser using nodeport and loadbalancer service.
exam--> http://node_ip:nodePort/war_file_name
        http://192.128.122.22:31000/file_name

  ----thank you
