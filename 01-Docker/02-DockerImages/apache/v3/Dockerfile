# Base Image 
FROM ubuntu:16.04 

# Maintainer of this image
MAINTAINER Amit Vashist <amitvashist7@outlook.com>

# Update the APT Repo 
RUN apt-get update 

# Install Apache Packages 
RUN apt-get install apache2 -y 

# Deploy Custom Web Page
COPY index.html /var/www/html/

# Port MetaData
EXPOSE 80

# Run Apache Server 
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND" ]
