FROM postgres:latest

ENV POSTGRES_USER db
ENV POSTGRES_PASSWORD db
ENV POSTGRES_DB db

COPY db.sql /docker-entrypoint-initdb.d/

EXPOSE 5432