1. Jenkins

docker run --rm --name jen -d -u root -p 8080:8080 -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v "$HOME":/home jenkinsci/blueocean

or

docker run -d --rm --name jen -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts

2. nginx

docker run --rm -d -p 80:80 --name my_image nginx

3. Java

docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp openjdk:7 javac Main.java

docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp openjdk:7 java Main

4. httpd

docker pull docker.io/httpd

docker run --rm -d --name test_web_server -p 8085:80 -v "$PWD"/website/:/usr/local/apache2/htdocs/ docker.io/httpd:latest

5. tomcat

docker run --rm --name tomcat -p 8080:8080 -v $PWD/test:/usr/local/tomcat/webapps/test -d tomcat

echo "hello world">test/hello.htm

http://localhost:8080/test/hello.htm

6. elasticsearch

docker run -d --name es -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.10.1

http://localhost:9200



