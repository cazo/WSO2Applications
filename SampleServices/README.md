# WSO2 ESB Sample Services

Este 'Sample', utiliza uma API REST no perfil ESB para se conectar a um serviço back-end REST (microservice) que é definido como um 'Endpoint' HTTP no ESB.Essa aplicação foi criada a partir do tutorial [Sending a Simple Message to a Service] disponibilizado na documentação do [WSO2 Enterprise Integrator]
   

# Equipe
  - Claudio Cardozo - Arquiteto de Software
  - Claudius Ibn - Desenvolvedor Java Senior
  - Luiz Moraes de Lima Neto - Desenvolvedor Java Senior


## Como criar o arquivo de deploy (*.CAR):

- Clique com o botão direito do mouse no projeto `SampleServicesCompositeApplication` e selecione a opção `Export Composite Application Project` no menu pop-up.

## Como Executar:

1. No seu navegador da Web, navegue até o console de gerenciamento do ESB usando a seguinte URL:  https://localhost:9443/carbon/.

2. Faça login no console de gerenciamento usando suas credenciais. As credenciais padrão são:

   ```
    Username: admin
    Password: admin
   ```

3. No painel de navegação esquerdo, clique em APIs no barramento de serviço (Service Bus/APIs). Aqui, você poderá ver listada a API REST criada neste projeto (HealthcareAPI). Esta API agora está pronta para receber solicitações e enviá-las para o serviço back-end. Aqui, você também poderá ver o URL de Invocação da API que deve ser usado para enviar a solicitação ao serviço.

    ![Deployed APIs](https://docs.wso2.com/download/attachments/85376682/Deployed%20API.png?version=1&modificationDate=1490333658000&api=v2)

4. Abra um terminal de linha de comando e insira a seguinte soicitação:

    ```bash
    curl -v http://localhost:8280/healthcare/querydoctor/surgery
    ```

5. Você verá a mensagem de resposta do 'HealthcareService' com uma lista de médicos disponíveis e os detalhes relevantes.

    ```bash
    [{"name":"thomas collins",
      "hospital":"grand oak community hospital",
      "category":"surgery",
      "availability":"9.00 a.m - 11.00 a.m",
      "fee":7000.0},
     {"name":"anne clement",
      "hospital":"clemency medical center",
      "category":"surgery",
      "availability":"8.00 a.m - 10.00 a.m",
      "fee":12000.0},
     {"name":"seth mears",
      "hospital":"pine valley community hospital",
      "category":"surgery",
      "availability":"3.00 p.m - 5.00 p.m",
      "fee":8000.0}
   ```

6. Agora, verifique o console do servidor do perfil ESB no Eclipse e você verá a seguinte mensagem:
   ```
    INFO - LogMediator message = "Welcome to HealthcareService"
   ```
    Esta é a mensagem impressa pelo mediador do Log criado neste projeto, quando a mensagem do cliente é recebida na seqüência do recurso da API.
  
[Sending a Simple Message to a Service]: <https://docs.wso2.com/display/EI611/Sending+a+Simple+Message+to+a+Service>
[WSO2 Enterprise Integrator]: <https://docs.wso2.com/display/EI611/Quick+Start+Guide>
