# kubernetes state metrics configs.ensure CRDs are installed first

1 - 
$ kubectl apply -f metrics-cluster-role-binding.yaml

2 - 
$ kubectl apply -f metrics-cluster-role.yaml


3 - 
$ kubectl apply -f metrics-service-account.yaml

4 - 
$ kubectl apply -f metrics-service.yaml

5 - 
$ kubectl apply -f metrics-deployment.yaml


Projetos de apoio

[Projeto de apoio](https://github.com/kubernetes/kube-state-metrics)
[Documetação oficial](https://kubernetes.io/blog/2021/04/13/kube-state-metrics-v-2-0/)