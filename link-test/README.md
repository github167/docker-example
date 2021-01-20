docker run --name mydb -e MYSQL_ROOT_PASSWORD=123456 -d mysql

docker run -d --link mydb:mysql -p 8080:8080 adminer


login adminer

Server:mydb

root:123456
