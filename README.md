# Adicionando-Seguran-a-em-APIs-na-AWS-com-Amazon-Cognito
Criar Projeto: Passo a passo.
Para criar um projeto com as características descritas, você pode seguir os seguintes passos:

1. **Amazon Cognito**:
    - Crie um **User Pool** no Amazon Cognito para gerenciar os usuários da sua aplicação. Isso permitirá que você adicione autenticação e autorização à sua API.
    - Configure os fluxos de autenticação, como login com e-mail/senha, login social (Facebook, Google, etc.) e autenticação multifator.
    - Defina as permissões de acesso para os usuários, como grupos e papéis.

2. **Amazon DynamoDB**:
    - Crie uma tabela no DynamoDB para armazenar os dados da sua aplicação. Por exemplo, se você está criando uma aplicação de notas, crie uma tabela para armazenar as notas dos usuários.
    - Defina a chave primária da tabela (por exemplo, `userId` e `noteId`).

3. **AWS Lambda**:
    - Crie funções Lambda para processar as operações da sua aplicação (criar, recuperar e excluir notas).
    - Configure as permissões das funções Lambda para acessar a tabela do DynamoDB.

4. **Amazon API Gateway**:
    - Crie uma API REST no API Gateway.
    - Crie recursos e métodos para as operações da sua aplicação (por exemplo, POST para criar uma nota, GET para recuperar notas, DELETE para excluir uma nota).
    - Configure a integração com as funções Lambda criadas anteriormente.

5. **Autorização com Amazon Cognito**:
    - Crie um autorizador no API Gateway para verificar os tokens de acesso gerados pelo Cognito.
    - Configure as políticas de autorização para permitir ou negar o acesso aos recursos da API com base nos grupos e papéis dos usuários.

6. **Teste sua API**:
    - Use o Postman ou outra ferramenta para testar as operações da sua API.
    - Verifique se a autenticação e autorização estão funcionando corretamente.

7. **Limpeza de recursos**:
    - Quando terminar de testar, não se esqueça de excluir os recursos criados (User Pool, tabela DynamoDB, funções Lambda, API Gateway, etc.) para evitar custos desnecessários.

https://github.com/cassianobrexbit/dio-live-cognito
