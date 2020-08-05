# Desafio em Automação de APIs

  Desafio utilizando as APIs do Facebook, foi desenvolvido conforme os seguintes pontos:
  
   - Análise e Escrita dos Cenários de testes em BDD. 
   - Automação dos cenários levantados, utilizando o Postman.
   - Execução dos testes e elaboração do relatório com o Newman.

### **Especificação de Requisito:**
   - O usuário deve realizar a autenticação no facebook.
                  (https://developers.facebook.com/docs/facebook-login/access-tokens).
   - O usuário deve postar uma mensagem na página desse mesmo usuário.
                  (https://developers.facebook.com/docs/graph-api/reference/v3.2/user/feed).
   - Realizar uma alteração na mensagem postada acima.
                  (https://developers.facebook.com/docs/graph-api/reference/v3.2/post#updating).

OBS: Devido à descontinuação da permissão publish_actions, não é mais possível usar a API para publicar publicações de usuário e/ou atualiza-las. Os testes foram desenvolvidos, se baseando na continuidade da permissão, e em erros de autenticação.

### **Testes**
  Foi criada uma Collection no Postman, contendo as validações dos cenários de teste e a utilização de Envaronmets, para o armazenamento de variáveis.
  
  Para a execução dos testes, foi utilizado o Newman, além de ser uma forma rápida de execução, é possível integrar com ambientes de CI/CD. 
  
      newman run "Desafio APIs Facebook.postman_collection.json" -e Facebook.postman_environment.json --reporters=cli,htmlextra

### **Relatórios**
Para a criar o layout em http, foi instalado HTML Report.

      npm install -g newman-report-htmlextra
      
Além do resultado do exibido no Prompt (Imagem 3) é possível visualiza-lo em [HTML](https://github.com/jaquelineantuness/DesafioAutomacao/tree/master/DesafioSensedia/newman).

   ![home_report_2](https://user-images.githubusercontent.com/25389211/58244022-2a19ab80-7d28-11e9-86dd-5ae88f531c07.png)
![total_request_report](https://user-images.githubusercontent.com/25389211/58244235-98f70480-7d28-11e9-83f3-dcbe4fecf68c.png)
![newman_report](https://user-images.githubusercontent.com/25389211/58244241-9b595e80-7d28-11e9-9b77-1e73a7e87b90.png)

    
