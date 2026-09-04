# Docker

```shell
docker ps
docker ps -a

docker image ls
docker pull postgres:15

docker run -it python:3.13-slim  # nom aleatoire : stoic_bouman
docker rm stoic_bouman 
docker run -it --rm python:3.13-slim # vigorous_swirles
docker run -it --rm python:3.10-slim # pull + run
docker run -it --rm python:3.10-alpine
docker run -it --rm python:3.10-slim bash

docker run --name pgdbmovie -e POSTGRES_PASSWORD=mysecretpassword -d postgres:18
docker exec -it pgdbmovie bash
    ls /var/lib/postgresql/18/docker/
    # base          pg_dynshmem    pg_logical    pg_replslot   pg_stat      pg_tblspc    pg_wal                postgresql.conf
    # global        pg_hba.conf    pg_multixact  pg_serial     pg_stat_tmp  pg_twophase  pg_xact               postmaster.opts
    # pg_commit_ts  pg_ident.conf  pg_notify     pg_snapshots  pg_subtrans  PG_VERSION   postgresql.auto.conf  postmaster.pid
    ps -aef
    # UID          PID    PPID  C STIME TTY          TIME CMD
    # postgres       1       0  0 12:52 ?        00:00:00 postgres
    # postgres      66       1  0 12:52 ?        00:00:00 postgres: io worker 0
    # postgres      67       1  0 12:52 ?        00:00:00 postgres: io worker 1
    # postgres      68       1  0 12:52 ?        00:00:00 postgres: io worker 2
    # postgres      69       1  0 12:52 ?        00:00:00 postgres: checkpointer 
    # postgres      70       1  0 12:52 ?        00:00:00 postgres: background writer 
    # postgres      72       1  0 12:52 ?        00:00:00 postgres: walwriter 
    # postgres      73       1  0 12:52 ?        00:00:00 postgres: autovacuum launcher 
    # postgres      74       1  0 12:52 ?        00:00:00 postgres: logical replication launcher 
    # root          81       0  0 12:56 pts/0    00:00:00 bash
    # root          90      81  0 12:56 pts/0    00:00:00 ps -aef
```