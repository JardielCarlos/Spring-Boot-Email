<h1 align="center" style="font-weight: bold;">Spring-Boot-Email 💻</h1>

<p align="center">
 <a href="#tech">Technologies</a> • 
<a href="#objective">Objective</a> • 
 <a href="#started">Getting Started</a> • 
  <a href="#routes">API Endpoints</a> •
 <a href="#colab">Collaborators</a> •
 <a href="#contribute">Contribute</a>
</p>

<p align="center">
    <b>Descrição simples do que o projeto faz e como usá-lo.</b>
</p>

<h2 id="technologies">💻 Technologies</h2>

- lista de todas as tecnologias usada
- Java
- Spring Boot
- Hibernate
- PostgreSQL
- RabbitMQ

<h2 id="objective">💡 Objective</h2>

Esse projeto tem o intuito de demonstra um micro-serviço utilizando Spring Boot e RabbitMQ no envio de email de uma aplicação no qual é enviado o email de maneira sincrona e de maneira assincrona (com RabbitMQ)

<h2 id="started">🚀 Getting started</h2>

- ### Como executar o projeto localmente.

<h3>Prerequisites</h3>

lista de todos os pré-requisitos necessários para execução do projeto.

- [Java](https://www.oracle.com/br/java/technologies/downloads/)
- [PostgreSQL](https://www.postgresql.org/download/)
- [RabbitMQ](https://www.rabbitmq.com/docs/download)

<h3>Cloning</h3>

Como clonar o projeto

```bash
git clone https://github.com/JardielCarlos/Spring-Boot-Email.git
```

<h3>Config .properties variables</h2>

Altere o arquivo `application.properties` colocando suas crendencias de configuração do banco de dados

```properties
server.port=8080

spring.datasource.url= jdbc:postgresql://localhost:{PORTA_BD}/{NOME_BD}
spring.datasource.username=USERNAME_BD
spring.datasource.password=SENHA_BD
spring.jpa.hibernate.ddl-auto=update

spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=email@gmai.com
spring.mail.password= SENHA_EMAIL_APP
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

spring.rabbitmq.addresses=URL_CONEXAO_RABBITMQ
spring.rabbitmq.queue=NOME_QUEUE
```

<h2 id="routes">📍 API Endpoints</h2>

lista das rotas da API e quais são os corpos de solicitação esperados.
​
| route | description  
|----------------------|-----------------------------------------------------
| <kbd>POST /sending-email</kbd> | Envia um email [detalhes do envio e resposta](#post-sendmail-detail)


<h3 id="post-sendmail-detail">POST /sending-email</h3>

**REQUEST**

```json
{
	"ownerRef": "João",
	"emailFrom": "joaoServicoMail@gmail.com",
	"emailTo": "pedro.lucena@hotmail.com",
	"subject": "Envio de email utilizando SMTP e SpringBoot",
	"text": "Envio realizado com sucesso do email com SpringBoot"
}
```

**RESPONSE**

```json
{
	"emailId": "3449b469-1c8b-4bfb-9e92-ef580d7eb46c",
	"ownerRef": "João",
	"emailFrom": "joaoServicoMail@gmail.com",
	"emailTo": "pedro.lucena@hotmail.com",
	"subject": "Envio de email utilizando SMTP e SpringBoot",
	"text": "Envio realizado com sucesso do email com SpringBoot",
	"sendDateEmail": "2024-03-13",
	"statusEmail": "SENT"
}
```

<h2 id="colab">🤝 Collaborators</h2>

Participantes do Projeto

<table>
  <tr>
    <td align="center">
      <a href="#">
        <img src="https://avatars.githubusercontent.com/u/88459973?v=4" width="100px;" alt="Jardiel Carlos Profile Picture"/><br>
        <sub>
          <b>Jardiel Carlos</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

<h2 id="contribute">📫 Contribute</h2>

Para contribuir para este projeto, siga os passos abaixo:

1. `git clone https://github.com/JardielCarlos/Spring-Boot-Email.git`
2. `git checkout -b feature/NAME`
3. Abra um Pull Request explicando o problema resolvido ou recurso realizado, se existir, anexe screenshot das modificações visuais e aguarde a revisão!

<h3>Documentações que podem ajudar</h3>

[📝 Como criar uma solicitação pull request](https://www.atlassian.com/br/git/tutorials/making-a-pull-request)
