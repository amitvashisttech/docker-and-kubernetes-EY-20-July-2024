  424  docker kill $(docker ps -q) 
  455  docker network ls
  456  docker network inspect 7daccc782664
  457  docker ps
  458  docker network ls

  425  docker ps
  426  docker images
  427  docker run -d --name job2 -p 8080:80  myapache:v5
  428  docker ps
  429  apt-get install net-tools -y
  430  netstat -tulnp
  431  curl 10.4.0.178:8080
  432  systemctl status docker
  433  docker run -d --name job3 -p 8080:80  myapache:v5
  434  docker run -d --name job4 -p 8081:80  myapache:v5
  435  docker ps
  436  docker run -d --name job5 -P  myapache:v1
  437  docker ps
  438  docker run -d --name job6 -P  myapache:v5
  439  docker ps
  440  systemctl status docker
  441  curl 10.4.0.178:32768
  442  ls
  443  docker run -d --name job7 -P  myapache:v4
  444  docker ps
  445  docker run -d --name job8 -P  myapache:v3
  446  docker ps




  467  docker kill $(docker ps -q)
  469  docker network ls
  470  docker ps
  471  docker run -it ubuntu # apt-get update ; apt-get install net-tools -y 
  472  Come Out : ctl p q 

# Let's Create a Custom Image with Network Utils
  473  docker commit -m "My Second Image" -p 0563f19dbaf0 mynetwork-ubuntu:v1
  474  docker ps
  475  docker images
  476  docker kill dazzling_lamarr
  477  ls
  478  docker run -itd --name default-nw-1 mynetwork-ubuntu:v1
  479  docker ps
  480  docker network ls
  481  docker run -itd --name host-nw-2 --network host mynetwork-ubuntu:v1
  482  docker run -itd --name none-nw-3 --network none mynetwork-ubuntu:v1
  483  docker ps
  484  docker exec -it default-nw-1 ifconfig
  485  docker exec -it host-nw-2 ifconfig
  486  docker exec -it none-nw-3 ifconfig



# Network

208  docker images
  209  docker run -itd --name test-nw-1 network-test:v1
  210  docker run -itd --name test-nw-2 network-test:v1
  211  docker run -itd --name test-nw-3 network-test:v1
  212  docker ps
  213  docker network ls
  214  docker network inspect bridge
  215  docker ps
  216  docker exec -it test-nw-1 ifconfig
  217  docker exec -it test-nw-2 ifconfig
  218  docker exec -it test-nw-3 ifconfig
  219  docker exec -it test-nw-1 route -n
  220  docker exec -it test-nw-2 route -n
  221  docker exec -it test-nw-3 route -n
  222  docker exec -it test-nw-3 ping -c2 172.17.0.1
  223  docker exec -it test-nw-3 ping -c2 172.17.0.2
  224  docker exec -it test-nw-3 ping -c2 172.17.0.3
  225  docker exec -it test-nw-3 ping -c2 172.17.0.4
  226  docker exec -it test-nw-3 ifconfig
  227  docker exec -it test-nw-3 ping -c2 172.17.0.4
  228  docker ps
  229  docker network ls
  230  docker run -itd --name test-nw-none-4  --network none network-test:v1
  231  docker run -itd --name test-nw-none-5  --network none network-test:v1
  232  docker ps
  233  docker exec -it test-nw-3 ifconfig
  234  docker exec -it test-nw-none-4 ifconfig
  235  docker exec -it test-nw-none-5 ifconfig
  236  docker exec -it test-nw-none-5 route -n
  237  docker exec -it test-nw-none-5 ping -c2 172.17.0.4
  238  docker ps
  239  docker network ls
  240  docker network inspect none
  241  docker network ls
  242  docker run -itd --name test-nw-host-6  --network host network-test:v1
  243  docker ps
  244* docker exec -it test-none-4 ifconfig
  245  docker exec -it test-nw-none-5 ifconfig
  246  docker exec -it test-nw-host-6 ifconfig
  247  ls
  248  docker network ls
  249  docker images
  250  docker run -d --name apache-test-1 amitvashist7/docker-and-kubernetes-ey-20-july-2024
  251  docker ps
  252  docker inspect apache-test-1
  253  curl 172.17.0.5/info.html
  254  route -n
  255  ip addr
  256  curl 172.17.0.5/info.html
  257  netstat -tulnp
  258  docker run -d --name apache-test-2 -p 8081:80 amitvashist7/docker-and-kubernetes-ey-20-july-2024
  259  docker ps
  260  netstat -tulnp
  261  systemctl  status docker
  262  docker run -d --name apache-test-3 -p 8082:80 amitvashist7/docker-and-kubernetes-ey-20-july-2024:v3
  263  docker run -d --name apache-test-4 -p 8082:80 amitvashist7/docker-and-kubernetes-ey-20-july-2024:v3
  264  netstat -tulnp
  265  docker run -d --name apache-test-5 -p 8082:80 amitvashist7/docker-and-kubernetes-ey-20-july-2024:v3
  266  docker run -d --name apache-test-6 -p 8082:80 amitvashist7/docker-and-kubernetes-ey-20-july-2024:v3
  267  netstat -tulnp
  268  docker run -d --name apache-test-7 -P  amitvashist7/docker-and-kubernetes-ey-20-july-2024:v3
  269  docker ps
  270  ls
  271  docker run -d --name apache-test-7 -P  amitvashist7/docker-and-kubernetes-ey-20-july-2024:v2
  272  docker run -d --name apache-test-8 -P  amitvashist7/docker-and-kubernetes-ey-20-july-2024:v2
  273  docker run -d --name apache-test-9 -P  amitvashist7/docker-and-kubernetes-ey-20-july-2024:v1


