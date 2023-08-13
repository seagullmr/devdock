FROM mysql:8.0

ADD startup /etc/mysql/startup

RUN chown -R mysql:root /var/lib/mysql/

CMD ["mysqld"]

EXPOSE 3306
