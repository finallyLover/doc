## docker 安装xxl-job

```

docker run -di -e PARAMS="--spring.datasource.url=jdbc:mysql://127.0.0.1:3306/xxl_job?Unicode=true&characterEncoding=UTF-8 --spring.datasource.username=root --spring.datasource.password=123456 --xxl.job.accessToken=pingzhuyan.test" \
-p 9001:8080 \
-v /usr/local/src/docker/xxl-job:/home/ubantu/logs/xxl-job \
--name xxl-job \
--privileged=true \
xuxueli/xxl-job-admin:2.4.0
```

