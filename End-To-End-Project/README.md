## Projeto Bike
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

1.  Para iniciarmos essa consulta foi necessária a utilizção de CTE (Common Table Expression) para união de duas tabelas (*bike_share_yr_0* e *bike_share_yr_1*) juntamente com o comando Union All que combina as duas tabelas sem eliminar nenhum dado duplicado.
2.  Na consulta principal foram selecionadas as colunas essenciais e realizados dois cálculos, que foram: O cálculo da receita gerado pelo número de ciclistas multiplicados pelo preço cobrado na viagem e o cálculo para retornar a diferença entre a receita total gerada pelos ciclistas e o custo de operação (COGS - Cost of Goods).
3.  Após tudo isso é o momento de realizar o LEFT JOIN que vai retornar todos os registros da tabela à esquerda (*CTE a*) para os correspondentes a tabela da direita (*cost_table b*). Se não houver correspondência os valores vão aparecer como NULL.
4.  A junção é feita baseada na coluna ano (*Yr*) que significa que está associando os custos de produção ao ano específico.  


* Execução
  
  ![](https://i.postimg.cc/NjC97bx1/Query.jpg)