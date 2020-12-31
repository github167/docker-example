1. Jenkins

docker run --rm --name jen -d -u root -p 8080:8080 -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v "$HOME":/home jenkinsci/blueocean

or

docker run -d --rm --name jen -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts

2. nginx

docker run --rm -d -p 80:80 --name my_image nginx

3. Java

docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp openjdk:7 javac Main.java

docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp openjdk:7 java Main
