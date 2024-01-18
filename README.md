# EAD - API COURSE

## Sobre o projeto
Projeto Decoder EAD - Arquitetura de microservices, tem como maior
objetivo colocar em prática todos os conceitos abordados.

Cada funcionalidade da plataforma é abordada como um serviço independente, promovendo flexibilidade e isolamento de responsabilidades.

### Alguns dos conceitos abordados ao longo do projeto
`Shared Database Pattern`
`Event Driven Pattern`
`Comunicação por Coreografia`
`Authentication e Authorization com JWT`
`Observability`
`SAGA Pattern`
`Cross
Cutting`
`Event Carried State Transfer Pattern`

### Desenho da solução
![Desenho da solucao ead](imagens/projeto.png)

## Sobre a API
O microservice `course` desempenha um papel central na gestão de cursos, módulos e lições na plataforma educacional "EAD". Suas principais funcionalidades incluem:

- **Cadastro de Cursos:** Permite a criação e registro de novos cursos na plataforma.

- **Gestão de Módulos e Lições:** Facilita a estruturação de cursos por meio da criação e organização de módulos e lições.

- **Obtenção de Usuários Autorizados:** Permite recuperar a lista de alunos de um determinado curso para um curso específico. Essa recuperação só pode ser feito por usuários autorizados.

- **Cadastro de Usuários em Cursos:** Facilita a inclusão de usuários em cursos.

## Endpoints

`GET ALL COURSES - http://localhost:8080/ead-course/courses`

`GET ONE COURSE - http://localhost:8080/ead-course/courses/{course_id}`

`POST COURSE- http://localhost:8080/ead-course/courses`

`DELETE COURSE - http://localhost:8080/ead-course/courses/{course_id}`

`UPDATE COURSE - http://localhost:8080/courses/{course_id}`

`POST MODULE - http://localhost:8080/courses/{course_id}/modules`

`GET ALL MODULES - http://localhost:8080/courses/{course_id}/modules`

`GET ONE MODULE - http://localhost:8080/courses/{course_id}/modules/{module_id}`

`DELETE MODULE - http://localhost:8080/courses/{course_id}/modules/{module_id}`

`PUT MODULE - http://localhost:8080/courses/{course_id}/modules/{module_id}`

`POST LESSON - http://localhost:8080/modules/{module_id}/lessons`

`GET ALL LESSONS - http://localhost:8080/modules/{module_id}/lessons`

`GET ONE LESSON - http://localhost:8080/modules/{module_id}/lessons/{lesson_id}`

`PUT LESSON - http://localhost:8080/modules/{module_id}/lessons/{lesson_id}`

`DELETE LESSON - http://localhost:8080/modules/{module_id}/lessons/{lesson_id}`

`GET ALL USERS BY courseId - http://localhost:8080/ead-course/courses/{course_id}/users`

`POST SUBSCRIPTION User in Course - http://localhost:8082/ead-course/courses/{course_id}/users/subscription`

## Tecnologias utilizadas
- Java 11
- Spring boot
- Maven
- Eureka Client
- Spring Logging
- Spring AMQP
- Spring Actuator
- Spring Circuit breaker Resilience4j
- Spring Log4j2
- Spring Postgresql
- Spring Lombok
- Spring Data JPA
- Spring Security
- jjwt

## Como executar o projeto
- Pré-requisitos: Java 11
- Ter os seguinte projetos em execução:
    - Service Registry
    - Config Server
    - Api Gateway

```bash
# clonar repositório
git clone https://github.com/alinepazz/sistema-ead-microservice-api-course.git

# entrar na pasta raiz do projeto

# executar o projeto
mvn spring-boot:run
```
### Autor
Aline Soares da Paz

https://www.linkedin.com/in/alinepazz/



