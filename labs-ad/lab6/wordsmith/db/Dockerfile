FROM postgres:16-alpine
ENV POSTGRES_DB=words \
    POSTGRES_USER=words \
    POSTGRES_PASSWORD=words \
    POSTGRES_HOST_AUTH_METHOD=trust
COPY words.sql /docker-entrypoint-initdb.d/
EXPOSE 5432
