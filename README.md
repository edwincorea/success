# success
# https://devopscube.com/what-is-docker/

docker build -t ecorea/success

docker run -d -p 8626:8626 ecorea/success

# Clean Up

docker stop $(docker ps -a -q --filter ancestor=ecorea/success)  
docker rm $(docker ps -a -q --filter status=exited)  
docker rmi ecorea/success