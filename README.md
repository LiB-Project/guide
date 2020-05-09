# Execução LiB-Project

## Requisitos
- Maven
- Java 8
- Docker
- Docker Compose
- python3
- pipenv
- Angular CLI 8

## Passo a passo para execução

### - Instância do Elasticsearch

    docker-compose up
    
### - [analysis-tool](https://github.com/LiB-Project/analysis-tool)

    sh run.sh


### - [back-end](https://github.com/LiB-Project/back-end)
Defina no arquivo ***application.yml*** as credenciais do super-usuario default, por padrão as credenciais são:

```yaml
credenciais:  
  login: "super-default"  
  senha: "default"  
  nome: "Super Usuário Default"
```
Altere conforme desejar para ter acesso a administração e configuração do sistema por meio do super usuário.


Após isso compile e execute o back-end

    mvn spring-boot:run

### - [web-app](https://github.com/LiB-Project/web-app)

    ng serve

### - Acessando a Interface de usuário

	http://localhost:4200 (Para acesso público)
	http://localhost:4200/login (Para acesso restrito)


