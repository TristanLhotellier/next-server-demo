FROM ubuntu

RUN apt-get update && apt-get install -y postgresql postgresql-contrib

EXPOSE 5432

CMD ["postgres", "-D", "/var/lib/postgresql/data"]