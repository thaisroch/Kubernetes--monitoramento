## Kubernetes Mysql exporter .


1- Aplicar o service no ambiente para o pod.

$ apply -f mysql-exporter-service.yaml

2 - Aplicar o deploymente do container exporter do mysql para o prometheus.

$ apply -f mysql-exporter-deployment.yaml


OBS. :  Deve ser modificado o arquivo adicionando as informaçoes no campos.

- name: DATA_SOURCE_NAME
  value: "USUARIO_BANCO:SENHA_BANCO@(CLUSTER_IP_BANCO:3306)/"

(https://github.com/prometheus/mysqld_exporter)
(https://github.com/prometheus/mysqld_exporter/tree/main/mysqld-mixin/alerts)