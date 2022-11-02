##  Para criar uma imagem docker

#### Após as configurações padrões no arquivo *Dockerfile*, selecione a pasta src e execute os seguintes comandos:
```bash
docker build -t seuUserDockerhub/conversao-temperatura:v1 .

```
#### Para verificar se a imagem foi criada:
```bash
docker image ls

```
#### Para excluir imagens "lixo":
```bash
docker image prune

```
#### Para subir para o DockerHub:
```bash
docker push seuUserDockerhub/conversao-temperatura:v1
```
- Não esquecer de subir a tag latest por padrão docker.
```bash
docker tag seuUserDockerhub/conversao-temperatura:v1 alexalexandrealves/conversao-temperatura:latest
docker push seuUserDockerhub/conversao-temperatura:latest
```

#### Para executar a imagem:
`-d`: Executa a imagem em modo daemon
#
`-p`: Efetua o portbind com a porta local

```bash
docker container run -d -p 8080:8080 alexalexandrealves/conversao-temperatura:v1

```
