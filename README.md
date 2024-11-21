# Redirecionador de URLs

### Este projeto é um dos serviços que compõem o encutador de URLs. Este é o serviço que faz o redirecionamento das URLs encurtadas para as URLs originais.

## Tecnologias Utilizadas
- Java 17
- Jackson
- Lombok
- Maven
- Postman
- AWS S3
- AWS lambda
- AWS API Gateway

## Como utilizar
### Execute a seguinte URL no navegador

```
https://6dsal8smxc.execute-api.us-east-2.amazonaws.com/{urlCode}
```

**urlCode:** Código referente a URL original gerado a partir da execução do seguinte endpoint(Necessário utilizar algum client http como o [Postman](https://www.postman.com/):

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

## Projetos relacionados
- [Gerador de URLs](https://github.com/url-shortener-project/url-shortener-generator)
  
