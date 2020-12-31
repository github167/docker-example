1. Jenkins

docker run --rm --name jen -d -u root -p 8080:8080 -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v "$HOME":/home jenkinsci/blueocean

2. nginx
docker run --rm -d -p 80:80 --name my_image nginx
