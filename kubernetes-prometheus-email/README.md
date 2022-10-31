## ☸️ kubernetes prometheus Setup

1- Aplique o clusterRole para export as metricas do ambiente.

$ kubectl apply -f prometheus-clusterRole.yaml

2- Aplicando o recurso configmap de configuração e de rule do prometheus

$ kubectl apply -f prometheus-configmap-config.yaml

$ kubectl apply -f prometheus-configmap-rules.yaml

Verificar o configmap com o comando:

$ kubectl get cm -n monitoring

3 - Aplicando o service do prometheus para obter acesso ao pod.

$ kubectl apply -f prometheus-service

Verificar o service e as informações de ip e as portas do prometheus

$ kubectl get svc -n monitoring

4 - Aplicando o pod do micro serviço do prometheus

$ kubectl apply -f prometheus-deployment.yaml

Verficiar com o comando 

$ kubectl get pods -n monitoring

$ kubectl get deploy -n monitoring

É possivel fazer acesso a ferramenta pelo browser.

$ kubectl get nodes -o wide

http://CLUSTER-IP:POTA-EXTERNA-POD

## Projeto de apoio.

[Documentação oficial Prometheus](https://prometheus.io/docs/prometheus/latest/getting_started/)
[Kubernetes Monitoting setup Using Prometheus](https://devopscube.com/setup-prometheus-monitoring-on-kubernetes/)
