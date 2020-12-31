Example 1:
docker build -t volumetest .

docker run --name vtest -it volumetest /bin/bash

touch /storage/hello.txt

docker inspect -f "{{.Mounts}}" vtest

check the exitence of the "hello.txt"

