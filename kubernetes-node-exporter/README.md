## Kubernetes node exporter setup


1 - Aplicando o service para configurar as informações de conexão do pod

$ kubectl apply -f node-service.yaml

1 - Criando os pods/deamonset de exporter do node.

$ kubectl apply -f node-deamonset.yaml




Projetos de apoio

[repositório de apoio](https://github.com/prometheus/node_exporter)
[Documentação oficial](https://prometheus.io/docs/guides/node-exporter/#node-exporter-metrics)
