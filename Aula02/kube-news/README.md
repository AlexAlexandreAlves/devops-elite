# Kubernets

## Cluster kubernetes, responsável pela criação de um cluster atrelado a um container

```bash
- k3d cluster create nomedocluster
- Cria com mais de um server e  mais de um agent: k3d cluster create meucluster --servers 3 --agents 3
```

#### Para visualizar e manipular todos os clusters existentes

```bash
- Visualiza: kubectl get nodes
- Lista: k3d cluster list
- Deleta: k3d cluster delete
- Visualizar as Api's do cluster: kubectl api-resources
```

## Pod - Responsável pela execução dos containers
#### Para criar e manipular um pod selecione o arquivo yaml de config no vscode e execute o comando
```bash
- Criar: kubectl create -f .\pod.yaml
- Visualizar: kubectl get pods
- Descrever detalhadamento: kubectl describe pod meupod
- Redirecionar a porta: kubectl port-forward pod/meupod 8080:80
```

## Deployment - Responsável pela criação e execução dos pods - Está acima na camada de gerenciamento
#### Para criar e manipular um deplyment selecione o arquivo yaml de config no vscode e execute o comando
```bash
- Criar: kubectl apply -f .\deployment.yaml
- Visualizar: kubectl get all
- Criando port-forward: kubectl port-forward service/postgre 5432:5432
```
