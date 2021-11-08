# Lab 11 - Amazon API Gateway

Em este lab sobre **API Gateway** aprenderemos alguns conceitos do API gateway da plataforma da AWS:
 - Configuração de rotas
 - *Throttling* (limitação do número de requisições por segundo) 
 - Monitoramento
 
## Pre-reqs

- Dois URLs accessíveis. Por exemplo, dois apps no Beanstalk:
    * http://springboot-env.eba-7znjbf9p.us-eats-1.elasticbeanstalk.com
        ![](img/api1.png)
    * http://springboot-env-1.eba-7zbhbf9p.us-east-1.elasticbeanstalk.com
        ![](img/api2.png)


 ## Configuração do serviço
 
1. Acessar o serviço **API Gateway**:
   ![](img/api3.png)

2. Criar uma nova API HTTP:
   ![](img/api4.png)

3. Configurar o nome da API e as integrações, apontando para as duas URLs dos prereqs usando o método `GET`:
   ![](img/api5.png)
   
4. Configurar as rotas, `/v1` apontando para uma URL e `/v2` apontando para a outra:
   ![](img/api6.png)

5. Sem modificações na configuração padrão de *stages*:
   ![](img/api7.png)
   
6. Revisar as configurações e confirmar a criação:
   ![](img/api8.png)
   
7. Aguardar a criação da API:
   ![](img/api9.png)

8. Testar a URL da API, a seguinte mensagem é normal pois não foi configurada a rota `/`:
   ![](img/api10.png)

9. Testar as rotas `v1` e `v2` da API:
   ![](img/api11.png)
   
   ![](img/api12.png)

10. Existe a possibilidade de limitar o número de requisições por segundo da API (*throttling*):
   ![](img/api13.png)

