# WSO2Applications

Repositório de 'Composite Applications' para o projeto de implantação do ESB WSO2 na 1001.

# Equipe
  - Claudio Cardozo - Arquiteto de Software
  - Luiz Moraes de Lima Neto - Desenvolvedor Java Senior

# Aplicações
Este repositório contém os seguintes WSO2 ESB Composite Applications:

- [Correio Services](/CorreioServices/)
   Aplicação de teste para serviço dos correios [AtendeCliente?wsdl]

- [Sample Services](/SampleServices/)
   Aplicação criada a partir do tutorial [Sending a Simple Message to a Service] disponibilizado na documentação do [WSO2 Enterprise Integrator]
   
## <a name="ExportToDevStudio"> Como importar os projetos para o Developer Studio:

1.  Abra um terminal de linha de comando e insira a seguinte soicitação para baixar ckonar o repositório
    ```bash
    git clone https://github.com/moraesdelima/WSO2Applications.git
    ```
2. Abra o Developer Studio e em seguida acesse a opção de menu `File/Import...`

    ![Import - Passo 01](/resources/images/import/import-passo-02.jpg)

3. No diálogo de importação selecione a opção `WSO2/Existing WSO2 Projects into workspace`

    ![Import - Passo 02](/resources/images/import/import-passo-03.jpg)
	
4. Informe em `Select root directory`, o diretório para onde o repositório foi baixado. Marque os projetos desejados, conforme abaixo, para a aplicação desejada e clique em Finalizar (Finish):

    - <NomeAplicaçãoWSO2>
    - <NomeAplicaçãoWSO2>CompositeApplication
    - <NomeAplicaçãoWSO2>ConnectorExporter
    - <NomeAplicaçãoWSO2>sRegistry
	
    ![Import - Passo 02](/resources/images/import/import-passo-04.jpg)
	
5. Como resultado os projetos serão importados para o seu workspace

    ![Import - Passo 02](/resources/images/import/import-passo-05.jpg)


[AtendeCliente?wsdl]: <https://apps.correios.com.br/SigepMasterJPA/AtendeClienteService/AtendeCliente?wsdl>
[Sending a Simple Message to a Service]: <https://docs.wso2.com/display/EI611/Sending+a+Simple+Message+to+a+Service>
[WSO2 Enterprise Integrator]: <https://docs.wso2.com/display/EI611/Quick+Start+Guide>