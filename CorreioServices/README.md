# WSO2Applications

Este projeto utiliza uma API REST ESB para se conectar a um serviço back-end SOAP dos correios que é definido como um 'Endpoint' HTTP no ESB. Aplicação para teste de conceito criada a partir do WSDL, [AtendeCliente?wsdl], dos correios 

# Equipe
  - Claudio Cardozo - Arquiteto de Software
  - Luiz Moraes de Lima Neto - Desenvolvedor Java Senior

## Como importar o projetos para o Developer Studio:

- Siga os passos definidos na raiz do repositório [WSO2 Applications](https://github.com/moraesdelima/WSO2Applications#ExportToDevStudio)

## Como criar o arquivo de deploy (*.CAR):

1. Clique com o botão direito do mouse no projeto `SampleServicesCompositeApplication` e selecione a opção `Export Composite Application Project` no menu pop-up.

2. No seu navegador da Web, navegue até o console de gerenciamento do ESB. URL para a instalação padrão:  https://localhost:9443/carbon/.

3. Faça login no console de gerenciamento usando suas credenciais. As credenciais para a instalação padrão são:

   ```
    Username: admin
    Password: admin
   ```

4. No painel de navegação esquerdo, clique em APIs no barramento de serviço (Service Bus/APIs). Aqui, você poderá ver listada a API REST criada neste projeto (HealthcareAPI). Esta API agora está pronta para receber solicitações e enviá-las para o serviço back-end. Aqui, você também poderá ver o URL de Invocação da API que deve ser usado para enviar a solicitação ao serviço.

    ![Deployed APIs](https://docs.wso2.com/download/attachments/85376682/Deployed%20API.png?version=1&modificationDate=1490333658000&api=v2)


[AtendeCliente?wsdl]: <https://apps.correios.com.br/SigepMasterJPA/AtendeClienteService/AtendeCliente?wsdl>