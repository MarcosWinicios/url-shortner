# Gerador de URLs

#### Este projeto é um dos serviços que compõem o encutador de URLs. Este é o serviço que recebe a armazena a URL original relacionando-a a uma código curto aleatório.

## Tecnologias Utilizadas
- Java 17
- Jackson
- Lombok
- Maven
- AWS S3
- AWS lambda
- AWS API Gateway

## Como utilizar
### Execute a seguinte URL em um cliente http, como o [Postman](https://www.postman.com/):

**Request**:

**POST** ``https://6dsal8smxc.execute-api.us-east-2.amazonaws.com/create``
```
  {
    "originalUrl":"https://github.com/MarcosWinicios",
    "expirationTime": "1732270940" //timestamp in seconds
  }
```
**Response**:
```
  {
      "code": "554bec03"
  }
```
Para testar a URL encurtada execute a seguinte URL no navegador, onde urlCode é o valor retornado no campo ``code`` da requisição anterior:

```
https://6dsal8smxc.execute-api.us-east-2.amazonaws.com/{urlCode}
```


## Projetos relacionados
- [Redirecionador de URLs](https://github.com/url-shortener-project/url-shortener-redirector)
