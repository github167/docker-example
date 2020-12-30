# docker-tomcat
From: https://ithelp.ithome.com.tw/articles/10192938
git clone
docker build -t tomcatserver .
docker run --rm -d --name tomcat -p 8080:8080 tomcatserver
docker inspect -f '{{.Mounts}}' tomcat
wget http://updates.jenkins-ci.org/download/war/2.273/jenkins.war

http://localhost:8080/jenkins

docker exec tomcat cat /root/.jenkins/secrets/initialAdminPassword
