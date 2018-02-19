# WSO2Applications

Este projeto utiliza uma API REST ESB para se conectar a um serviço back-end SOAP dos correios que é definido como um 'Endpoint' HTTP no ESB. Aplicação para teste de conceito criada a partir do WSDL, [AtendeCliente?wsdl], dos correios 

# Equipe
  - Claudio Cardozo - Arquiteto de Software
  - Luiz Moraes de Lima Neto - Desenvolvedor Java Senior

## Como importar o projetos para o Developer Studio:

- Siga os passos definidos na raiz do repositório [WSO2 Applications](https://github.com/moraesdelima/WSO2Applications#ExportToDevStudio)

## Como criar o arquivo de deploy (*.CAR):

- Clique com o botão direito do mouse no projeto `CorreioServicesCompositeApplication` e selecione a opção `Export Composite Application Project` no menu pop-up.

## Como realizar o deploy

1. No seu navegador da Web, navegue até o console de gerenciamento do ESB. URL para a instalação padrão:  https://localhost:9443/carbon/.

2. Faça login no console de gerenciamento usando suas credenciais. As credenciais para a instalação padrão são:

   ```
    Username: admin
    Password: admin
   ```

3. Click the Main tab on the Management Console, go to Manage -> Carbon Applications and then click Add.
The Add Carbon Applications screen appears.

4. Click Choose File, select your CAR file and click Upload.
The CAR files that you upload are dropped to the <PRODUCT_HOME>/tmp/carbonapps/{tenant-ID}/ directory.

5. Refresh the browser to see that the CAR file has been deployed.

6. Click the Main tab on the Management Console, go to Manage -> Carbon Applications and then click List. If successfully deployed, the CAR file appears here.

7. No painel de navegação esquerdo, clique em APIs no barramento de serviço (Service Bus/APIs). Aqui, você poderá ver listada a API REST criada neste projeto (ConsultarCEP). Esta API agora está pronta para receber solicitações e enviá-las para o serviço back-end. Aqui, você também poderá ver o URL de Invocação da API que deve ser usado para enviar a solicitação ao serviço.

    ![Deployed APIs](https://docs.wso2.com/download/attachments/85376682/Deployed%20API.png?version=1&modificationDate=1490333658000&api=v2)


[AtendeCliente?wsdl]: <https://apps.correios.com.br/SigepMasterJPA/AtendeClienteService/AtendeCliente?wsdl>