ARG MYSQL_VERSION

FROM mysql:${MYSQL_VERSION}

COPY /mysql/my.cnf /etc/mysql/conf.d/my.cnf

RUN chown -R mysql:root /var/lib/mysql/