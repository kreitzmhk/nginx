docker run --name nginx1 -d nginx1:0.0.1
docker run --name nginx2 -d nginx2:0.0.1
docker run --name nginx3 -d nginx3:0.0.1

docker run -p 80:80 --link nginx1 --link nginx2 --link nginx3  --name "proxy" -d apache-proxy:0.0.4
