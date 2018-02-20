# WSO2Applications

Este projeto utiliza uma API REST ESB para se conectar a um serviço back-end SOAP dos correios que é definido como um 'Endpoint' HTTP no ESB. Aplicação para teste de conceito criada a partir do WSDL, [AtendeCliente?wsdl], dos correios 

# Equipe
  - Claudio Cardozo - Arquiteto de Software
  - Luiz Moraes de Lima Neto - Desenvolvedor Java Senior

## Como importar o projetos para o Developer Studio:

- Siga os passos indicados na raiz do repositório [WSO2 Applications](https://github.com/moraesdelima/WSO2Applications#ExportToDevStudio)

## Como criar o arquivo de deploy (*.CAR):

- Clique com o botão direito do mouse no projeto `CorreioServicesCompositeApplication` e selecione a opção `Export Composite Application Project` no menu pop-up.

## Como realizar o deploy

1. No seu navegador da Web, navegue até o console de gerenciamento do ESB. URL para a instalação padrão:  https://localhost:9443/carbon/.

2. Faça login no console de gerenciamento usando suas credenciais. As credenciais para a instalação padrão são:
   - Username: admin
   - Password: admin

3. Clique na guia Principal no Console de Gerenciamento, vá em `Manage` -> `Carbon Applications` e clique em `Add`.
	- A tela `Add Carbon Applications` aparece.

4. Clique em `Choose File`, selecione seu arquivo de deploy e clique em `Upload`.
   - Os arquivos CAR que você carrega são descartados no diretório <PRODUCT_HOME>/tmp/carbonapps/{tenant-ID}/.

5. Atualize o navegador para ver se o arquivo CAR foi implantado; OU Clique na guia Principal no Console de Gerenciamento, vá em  Manage -> Carbon Applications e clique em List. Se implementado com sucesso, o arquivo CAR aparece aqui.

6. No painel de navegação esquerdo, clique em APIs no barramento de serviço (Service Bus/APIs). Aqui, você poderá ver listada a API REST criada neste projeto (ConsultarCEP). Esta API agora está pronta para receber solicitações e enviá-las para o serviço back-end. Aqui, você também poderá ver o URL de Invocação da API que deve ser usado para enviar a solicitação ao serviço.

    ![Deployed APIs](https://docs.wso2.com/download/attachments/85376682/Deployed%20API.png?version=1&modificationDate=1490333658000&api=v2)

## Como Executar:

1. Abra um terminal de linha de comando e insira a seguinte soicitação:

    ```bash
    curl -v http://localhost:8280/atendeCliente/consultaCEP/22221010
    ```

2. Você verá a mensagem de resposta do 'HealthcareService' com uma lista de médicos disponíveis e os detalhes relevantes.

    ```bash
    {
		"consultaCEPResponse":{
			"return":{
				"bairro":"Catete",
				"cep":22221010,
				"cidade":"Rio de Janeiro",
				"complemento":null,
				"complemento2":"- at├® 99999 - lado ├¡mpar",
				"end":"Rua Bento Lisboa",
				"id":0,
				"uf":"RJ"
			}
		}
	}
   ```

[AtendeCliente?wsdl]: <https://apps.correios.com.br/SigepMasterJPA/AtendeClienteService/AtendeCliente?wsdl>