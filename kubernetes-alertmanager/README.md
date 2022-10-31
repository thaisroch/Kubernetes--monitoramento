# kubernetes alertmanager setup

1 - Aplicando o service do alertmanager para obter acesso ao pod.

$ kubectl apply -f alertmanager-service

Verificar o service e as informações de ip e as portas do grafana

$ kubectl get svc -n monitoring

2- Aplicando o configmap de template do email do alertmanager

$ kubectl apply -f alertmanager-configmapTemplate.yaml

3 - Aplicando o configmap de configuração do canal de saída do alertmanager

Obs.: Tem que ser adicionada as informações do gmail, apontando para a conta do google gmail desejada.
- Criação uma senha app dentro do gmail;
- modificação das configurações, sendo indicada no arquivo por ADD_AQUI.

$ kubectl apply -f alertmanager-configmapConfig.yaml

Verficiar o configmap com o comando

$ kubectl get cm -n monitoring

4 - Aplicando o deploy da ferrramenta no ambiente

$ kubectl apply -f alertmanager-deployment.yaml

Verificar o status do deploy

$ kubectl get deploy -n monitoring

Verificar o status do pod

$ kubectl get pod -n monitoring

É possivel fazer acesso a ferramenta pelo browser.

$ kubectl get nodes -o wide

http://CLUSTER-IP:POTA-EXTERNA-POD

Projeto de apoio.

[Documentação oficial  alertmanager](https://prometheus.io/docs/alerting/latest/alertmanager/)