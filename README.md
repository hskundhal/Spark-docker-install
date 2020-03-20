## Environment
Makes you running with spark as docker containers in master slave config

The provided `docker-compose.yml` and Spark configurations in `conf` directory are cloned from <https://github.com/gettyimages/docker-spark>.

## Install Instructions

0. Make sure Docker is installed and also `docker-compose` is ready to use
1. Run `$ docker-compose up -d` under the $$  directory
2. Check Spark UI at `http://localhost:8080` .There will be 1 master and 1 worker
3. Run `$ docker exec -it dockername /bin/bash` to get into the container shell and able to run  `spark-shell`, `pyspark` or `spark-submit` at terminal.

