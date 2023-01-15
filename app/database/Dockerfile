FROM postgres:15.1-alpine
ADD init-user-db.sh /
RUN chmod 777 init-user-db.sh
RUN ./init-user-db.sh
COPY ./postgresql.conf /etc/postgresql/