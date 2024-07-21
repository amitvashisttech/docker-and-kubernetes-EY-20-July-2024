# Base Image 
FROM ubuntu:noble 

# Owner of the Image 
MAINTAINER Amit Vashistha <amitvashist.tech@gmail.com>

# Update APT Repos
RUN apt-get update 

# Install Apache2 Packages from APT Repo. 
RUN apt-get install apache2 -y 

# Excute the Application Service 
CMD [ "/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
