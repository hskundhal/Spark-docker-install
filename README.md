## Environment
Makes you running with spark as docker containers in master slave config

The provided `docker-compose.yml` and Spark configurations in `conf` directory are cloned from <https://github.com/gettyimages/docker-spark>.

## Install Instructions

0. Make sure Docker is installed and also `docker-compose` is ready to use
1. Run `$ docker-compose up -d` under the main  directory
2. Check Spark UI at `http://localhost:8080` .There will be 1 master and 1 worker as shown by docker ps
`CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                                                                                                           NAMES
9f529ef2a9b0        gettyimages/spark   "bin/spark-class org…"   12 seconds ago      Up 8 seconds        7012-7016/tcp, 8881/tcp, 0.0.0.0:8081->8081/tcp                                                                 spark-docker-setup_worker_1
3d6538c195dd        gettyimages/spark   "bin/spark-class org…"   16 seconds ago      Up 11 seconds       0.0.0.0:4040->4040/tcp, 0.0.0.0:6066->6066/tcp, 0.0.0.0:7077->7077/tcp, 0.0.0.0:8080->8080/tcp, 7001-7006/tcp   spark-docker-setup_master_1`
3. Run `$ docker exec -it dockername /bin/bash` to get into the container shell and able to run  `spark-shell`, `pyspark` or `spark-submit` at terminal.

