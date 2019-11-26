FROM postgres:10.4-alpine
# Camunda BPM 7.10.x is supported on PostgreSQL 10.4
# See also: 
#   https://docs.camunda.org/manual/latest/introduction/supported-environments/
#   https://github.com/camunda-consulting/docker-camunda-platform/blob/master/postgres-camunda-ee/Dockerfile

COPY *.sql /docker-entrypoint-initdb.d/
RUN chmod -R 777 /docker-entrypoint-initdb.d