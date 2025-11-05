git 

Credential Manager → Windows Credentials
If any related to git remove it.

git init
git add .
git commit -m "Initial Commit"
git remote -v (Check if there are any previous accounts)
if there
git remote remove origin (the name)
git remote add origin (link from your repository)
git config --global user.name "Vangeli"
git config --global user.email "mail"

git push -u origin main
Sign with code




Experiment-4



How to download jenkins

Make the java version has 17 or 21
If not download java

If another version is there go to control panel and delete and download the new version

Click Jenkins download

Select windows

jenkins.msi will be start downloads

After download open it

A pop will display like Welcome to Jenkins
Click on Next

A path of Jenkins will be displayed don't change anything click on Next (C:\Program Files\Jenkins)

Select Run Service as LocalSystem (most recommended) and then click on next

Select port number and click Next

Paste the java path and click Next

It will display File structure click next

Click Install
Go to local browser and click [localhost:portnumber]

It will ask to enter the password

Copy the file path which is showed at first on the browser and password will be displayed so paste here.

Select "Install suggested plugins"

As all the plugins will be installed

Enter your details like username, password, full name, mail

Select default Jenkins URL and click on save and finish

Click on start using Jenkins

After installation click Finish





docker commands




docker pull hello-world (image name)
output:
default tag : latest
latest : Pulling from library/hello-world


for get all the images

To check whether it has images or not
docker images
output:
Repository TAG Image ID CREATED SIZE
hello-world latest 56x33      2034x

To run the container
docker run -d --name hello(container-name) helloworld(image-name)
output
c2726d7

To see the container ID
docker ps -a
CONTAINER ID IMAGE   COMMAND   CREATED STATUS PORTS NAMES
c2763 h   ello-world "/hello"          Exited       hello

To delete the container
docker rm hello hello-world

To delete the image
docker rmi hello-world



exp 7
docker containerized application

code is in dockerapp

in new terminal 

docker build -t hello .

docker run --name hellocontainer hello
it will give output Hello world

docker tag image-name user-name/reponame:latest

docker login

docker push username/imagename:latest




exp 8
kubernets integrate with docker

link is https://dl.k8s.io/release/v1.32.2/bin/windows/amd64/kubectl-convert.exe

kubectl version --client

kubectl get pods






Experiment - 9 docker deply

Write:
Test.java
Docker file

docker build -t image-name .

docker run --name container-name image-name

docker tag imagename username/reponame:latest

docker login

docker push username/imagename:latest

Add deployment.yaml / service.yaml

kubectl apply -f deployment.yaml
output  deployment.apps/my-java-app unchanged

kubectl apply -f service.yaml
output  service/my-java-app-service unchanged

kubectl get deployments


kubectl ge pods

kubectl get svc

fort ouput localhost:(nodePort in service.yaml)
