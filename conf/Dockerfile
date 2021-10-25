FROM httpd:latest

RUN apt update; \
    apt upgrade;


RUN apt install -y apache2 


#RUN a2enmod auth_digest
#RUN touch /etc/apache2/claves.txt
#RUN htdigest -c /etc/apache2/claves.txt grupo1 bilbo

#RUN chmod 640 /etc/apache2/claves.txt
#RUN chown root.www-data /etc/apache2/claves.txt

# Copy apache vhost file to proxy php requests to php-fpm container
COPY sri.asir4all.ss.conf /usr/local/apache2/conf/sri.asir4all.ss.conf
RUN echo "Include /usr/local/apache2/conf/sri.asir4all.ss.conf" \
    >> /usr/local/apache2/conf/httpd.conf
