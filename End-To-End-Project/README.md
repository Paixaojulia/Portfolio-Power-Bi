# Projeto Bike
### Overview do projeto

Esse projeto é um projeto de início ao fim (*End To End*), onde vou desde a construção do Banco de Dados até a criação do Dashboard. Foram utilizados as plataformas SQL Server Management Studio e o Power Bi. O projeto gira em torno dos dados adquiridos de 2 anos de uma loja de bicicletas. 


![](https://i.postimg.cc/90wRy3hz/Bike-dash.jpg)


## Introdução 
Para iniciar esse projeto decidi escolher o SQL Server para ser meu gerenciador de Banco de Dados. A sua instalação foi realizada de forma local no meu computador. 

## Instalação SQL Server 

* Para realizar o Download do SQL Server iremos clicar nesse [link](https://www.microsoft.com/pt-br/sql-server/sql-server-downloads) e selecionar a opção **Express**. 
![Imagem](https://i.postimg.cc/kgxgP9cJ/Download-SQL-Server-EXPRESS.jpg)

* Após a instalação ser concluída podemos apertar o botão **Install SSMS**, em seguida seremos direcionados para a seguinte [página](https://learn.microsoft.com/pt-br/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16&redirectedfrom=MSDN). Assim iremos baixar o SSMS em sua útlima versão atualizada. Quando sua instalação for concluída podemos escolher o local desejado e seguir com a finalização da instalação.

![](https://i.postimg.cc/T2N87Pz8/SQL-Server-Instalado.jpg)

 * Quando tudo for concluído, abra o app e certifique-se que as opções estão corretas, não se esqueça de marcar o box "Certificado do Servidor Confiável" e clique "Conectar". 
   
   ![](https://i.postimg.cc/Gt83qgxV/Servidor-confi-vel.jpg)

## Importação Banco de Dados

* Para iniciarmos a importação do Banco de Dados é necessário criar clicar com o botão direito na pasta **Banco de Dados**, adicionar o nome e selecionar "Ok".
  
  ![](https://i.postimg.cc/L8K4VM0M/Bike-data.jpg)
* Ao clicar com o botão direito no nosso Banco de dados, devemos selecionar "Tarefas" e "Importar Arquivo Simples". Na aba "Introdução" selecionar "Próxima" e assim procurar o caminho do arquivo desejado. Selecionar "Próxima" novamente e desmarcar o box "Usar Detecção de Tipos de Dados Avançados". Selecionar "Próxima" novamente e mais uma vez, em seguida selecionar "Concluir" e fechar.
  
  ![](https://i.postimg.cc/RCGcN2Sm/Visualizar-dados.jpg)
  
## Explicando e executando a Query 

* Para iniciar essa Query irei utilizar uma CTE (years_union) para combinar duas tabelas de anos diferentes, bike_share_yr_0 e bike_share_yr_1. Utilizei o famoso comando *UNION ALL* para combinar os dados, lembrando que ele não remove os dados duplicados. 


![](https://i.postimg.cc/GhtH3VYv/With-cte.jpg)


* Na segunda parte do código fiz um *LEFT JOIN* entre as tabelas years_union (CTE) e a tabela cost_table com objetivo de trazer os valores de custo, uni utilizando a chave yr.  Com isso criei três colunas, revenue, profit, Total_Cost e trouxe as colunas necessárias.
   * **revenue**: Tem o objetivo de trazer a receita multiplicando o número de ciclistas (riders) pelo preço cobrado na viagem (price).
   * **profit**: Possui o objetivo de trazer o lucro, calculando a diferença entre a receita total (profit) e o custo da operação (COGS - Cost of Goods)
   * **Total_Cost**: Seu objetivo é trazer o custo total, calculando a multiplicação do custo x corrida.
     
 ![](https://i.postimg.cc/66vyF5Jm/select.jpg)    


  ## Conexão ao Power Bi

  1- Para realizarmos a conexão ao Power Bi é bem simples. Basta entrar na aba "Página Inicial" e em seguida entrar em "Obter Dados" e após SQL Server. 
  
  2- No SQL Server iremos clicar com o botão direito no nome do nosso banco de dados e selecionar "Conectar", copiar o "Nome do Servidor" e inserir na aba "Servidor" dentro no Power Bi. 
  
  3- Manter o modo "Import" no Modo de conectividade de Dados, abrir a aba "Opções Avançadas" logo abaixo e inserir a "Instrução SQL" que será a nossa consulta que acabamos de criar. Continuaremos com o box de "Adicionar colunas de relação" marcado e seguir com o Ok.
  
  4- Na aba Banco de dados SQL Server que vai abrir vamos manter as configurações já pré definidas e selecionar "Conectar", marcar "Ok" e após "Carregar". 
  
  ![](https://i.postimg.cc/QCRBfmCk/Conect-Server.jpg)

  ## Estrutura da Base de Dados

A Base de Dados que importamos contém as seguintes colunas:

   * dteday
   * season
   * yr
   * weekday
   * hr
   * rider_type
   * riders
   * price
   * COGS
   * Revenue
     
As medidas **Custo Total**, **Lucro Total**, **Margem de Lucro**, **Média Receita**, **Receita Total**, **Total de Aluguéis** e **Total de Clientes** foram geradas a partir das demais colunas.

Quantidade de dados: 34.758 Linhas


  ## Organização com o método Kanban
  
Para realizar um projeto completo, um método de organização eficiente é essencial. A primeira etapa é o levantamento de requisitos, seguindo um processo bem definido para cada fase do projeto. Escolhi o **Kanban** como metodologia ágil devido à sua visualização clara através de quadros, que permite organizar as tarefas de forma intuitiva. O Kanban também oferece um fluxo contínuo de trabalho, facilitando a priorização e a execução das atividades, garantindo o acompanhamento e a conclusão das entregas de maneira estruturada e progressiva.

  ![](https://i.postimg.cc/ZKNfDZrh/Kanban.jpg)

  
  # Iniciando o Dashboard

  ## KPIs que foram exploradas:
  
 * **Receita**: O total de receita gerada no período de 2 anos foi 15,19M.
 * **Lucro**: O lucro da empresa é de 10,45M.
 * **Custo**: O custo de serviço da empresa é o total de 4,74M.
 * **Total de Clientes**: A quantidade de clientes distintos é de 776.
 * **Aluguéis**: O número de aluguéis de bicicleta foi de 3M. 
 * **Margem de Lucro**: A margem de lucro ficou em 68,80%.

   ## Insights e acionáveis:

 *  **Aumento de movimentação**:

Observa-se que os horários de maior movimentação na loja é entre às 7h até 10h e entre 16h até 20h. O horários que trazem maior receita na loja fazem sentido com a maioria das rotinas dos clientes que possivelmente estariam indo para escola, trabalho ou até em um momento de lazer no parque mais próximo. Um bom acionável para tornar os horários não tão movimentados em lucrativos são campanhas de marketing com promoções nos horários atípicos, assim incentivando o maior uso das bicicletas. 

* **Otimização de Custos e Eficiência Operacional**:

Apesar da margem de lucro já estar em um bom nível, é sempre bem vindo a revisão de custos fixos e variáveis para buscar oportunidades de redução ainda maior, principalmente em razão dos meses de baixa demanda.

* **Aumento de clientes registrados**:

A maior parte dos aluguéis é feita por clientes já registrados **(81,2%)**, que chama atenção pela loja ter uma base de clientes fiéis. A parte dos clientes casuais se trata de apenas **(18,8%)**, sendo assim se encontra uma necessidade de criação de promoções e pacotes para atração de clientes, possivelmente até programas de fidelização do cliente. 


* **Melhoria de Desempenho em Baixa Temporada:**  

O gráfico de barras indica o baixo índice de aluguéis de bicicleta na temporada de inverno, evidenciando uma sazonalidade também no mercado. Nos meses de alta demanda, deve-se investir em marketing para aproveitar a popularidade do aluguel de bicicletas, focando no público que busca atividades ao ar livre. 


  ## Finalização

  Por fim finalizamos o processo de criação auxiliado pelo método Kanban! E assim ficou o meu quadro de organização:

  ![](https://i.postimg.cc/Y2T1rhdw/Kanban-final.jpg)
  
