
# docker-airflow

```yaml
# docker-compose.yml
---
airflow_data:
  image: cheine/airflow
  entrypoint: /bin/true
  volumes:
    - ./airflow.cfg:/airflow/airflow.cfg:ro

airflow:
  image: cheine/airflow
  restart: always
  volumes_from:
    - airflow_data
  ports:
    - 127.0.0.1:9090:808
```
