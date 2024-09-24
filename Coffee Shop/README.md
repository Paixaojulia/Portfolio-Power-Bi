# Dashboard Loja de Café

![](https://i.postimg.cc/fbYZpyZ2/Screenshot-1.jpg)

## Overview do projeto

Esse projeto foi realizado apenas utilizando a plataforma Power Bi, trazendo um Dashboard que contém analises de venda de uma cafeteria. 

A base de dados contém informações valiosas que nos ajudam a otimizar as operações, crescimento de vendas e acentuar a satisfação do cliente. Segue um breve resumo do que podemos extrair da base de dados: 

1. Data e hora: Possuímos o registro de data e a hora de cada pedido, o que nos permite analisar o comportamento do cliente e identificar possíveis horários de pico.
2. Detalhes do pagamento: Detemos de cada detalhe do meio de pagamento, assim podemos identificar as preferências dos clientes tanto no tipo de produto e frequência. 



## Estrutura da Base de dados 

A estrutura da base de dados pode ser conferida através desse [link](https://www.kaggle.com/datasets/ihelon/coffee-sales/data)

O arquivo em excel contém as seguintes colunas: 
* Data
* Data e horário
* Meio de pagamento
* Numeração do cartão
* Valor do produto
* Variação do produto
  
As medidas **Quantidade de Vendas**, **Ticket Médio** e **Total de Vendas** foram geradas a partir das demais colunas. 

Quantidade de dados: 1.208


## Insights e Acionáveis 

**Identificação dos Best-sellers**: De acordo com a análise dos dados os produtos que mais venderam foram: **Latte, Americano With Milk, Cappuccino**. Seus valores em vendas foram respectivamente **9,5k, 9,3k e 7,8k**. O gráfico utilizado para realizar a análise foi o **Gráfico de barras empilhadas**. ![Gráfico de barras empilhadas](https://i.postimg.cc/Cxm61V7h/Screenshot-3.jpg)

**Recorrência de clientes**: Acompanhar a frequência de compra por cliente ao longo do tempo por transação a sua regularidade em cada mês, hora e pedido. O gráfico utilizado para realizar a análise foi o **Gráfico de barras empilhadas**.

**Análise de Receita e Sazonalidade**: Avaliar o total de receita gerada ao longo do ano oferece uma visão clara do desempenho financeiro. Além disso, é possível identificar padrões sazonais, entendendo os períodos de maior e menor volume de vendas, para otimizar o planejamento estratégico. O gráfico utilizado para realizar a análise foi o **Matriz**.

**Receita por Dia da semana e Hora**: 
* Os horários de pico de venda são concentrados entre 8h e 10h, com maior receita gerada às 8h (R$ 4,5 mil) e 9h (R$ 5,4 mil). Esses horários coincidem com o café da manhã, mostrando que a loja é mais movimentada nesse período. 
* Aos sábados e domingos as vendas caem em relação aos dias úteis, sugerindo que o público alvo da cafeteria seja composto por estudantes ou trabalhadores, que frequentariam aos dias de semana. 


## KPIs que foram exploradas:

* **Total da receita**: Total de receita gerada no período observado foi de 39.656,78.

* **Quantidade de Vendas**: 1.208 Total de pedidos realizados.

* **Ticket médio**: Ticket médio das vendas é de 32,83. 

* **Produto com maior rotatividade**: Produto que foi campeão de vendas no cardápio foi o Latte.

* **Receita por produto**: Com a análise correta dos dados, é possível identificar quais produtos são os mais vendidos. Com essa informação, a empresa pode aplicar estratégias de marketing direcionadas, como promoções e campanhas específicas, para impulsionar ainda mais as vendas desses itens. 

* **Quantidade de transação por meio de pagamento**: A grande parte das transações foram realizadas por meio de cartão (92,63%) e a outra parte com apenas 7,37%. 

* **Quantidade de transação por cliente**: Demonstra a frequência de um cliente com total de transações, meio de pagamento, pedido e horário.

* **Clientes não recorrentes**: O dashboard mostra uma lista de 89 clientes não recorrentes, transmitindo um alto número de clientes não fidelizados, que podem assim chamar a atenção de estratégias de fidelização. 

 

