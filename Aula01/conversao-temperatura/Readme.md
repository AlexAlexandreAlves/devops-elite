##  Para criar uma imagem docker

#### Após as configurações padrões no arquivo *Dockerfile*, selecione a pasta src e execute os seguintes comandos:
```bash
docker build -t seuUserDockerhub/conversao-temperatura:v1 .

```
#### Para verificar se a imagem foi criada:
```bash
docker image ls

```
#### Para excluir imagens lixo:
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

#### Para executar a imagem e listar a imagem criada:
- `-d`: Executa a imagem em modo daemon
- `-p`: Efetua o port binding com a porta local

```bash
docker container run -d -p 8080:8080 seuUserDockerhub/conversao-temperatura:v1
docker image ls

```

#### Se tudo der certo a aplicação deverá rodar assim:

![Captura de tela de 2022-11-01 22-01-52](https://user-images.githubusercontent.com/70979408/199370890-2ab12f76-4011-40ac-82cd-4293073dfd9b.png)
--
#### DockerHub
![Captura de tela de 2022-11-01 22-08-42](https://user-images.githubusercontent.com/70979408/199371070-6bc64a61-f874-4245-a30e-e91e711bfc86.png)
