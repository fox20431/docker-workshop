# Postgres

ref: https://github.com/docker-library/postgres/blob/master/15/bullseye/docker-entrypoint.sh

Change `timezone` and `log_timezone` of `postgresql.conf` from `Etc/UTC` to `Asia/Shanghai`.

In order to add the configuration, I modified the Dockerfile to copy the file to the container. However, it is now allowed to add the original path directly, because it asks whether the directory is empty or not. Then I used `docker-entrypoint.sh` which is used by `CMD` to copy it to the correct path.