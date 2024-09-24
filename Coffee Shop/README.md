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

**Identificação dos Best-sellers**: De acordo com a análise dos dados os produtos que mais venderam foram: **Latte, Americano With Milk, Cappuccino**. Seus valores em vendas foram respectivamente **R$ 9,5 mil, R$ 9,3 mil e R$ 7,8 mil**. O gráfico utilizado para realizar a análise foi o **Gráfico de barras empilhadas**. Com base na identificação dos best-sellers, a loja pode focar em promover os produtos **Latte, Americano With Milk e Cappuccino** com campanhas direcionadas, ofertas especiais ou combos, além de garantir estoque adequado desses itens para manter a alta demanda.

![](https://i.postimg.cc/Cxm61V7h/Screenshot-3.jpg)

**Recorrência de clientes**: Para verificação da frequência dos clientes utilizei o final do cartão do cliente, pois era o único dado disponível para o cálculo dessa métrica. Podemos observar de acordo com o gráfico que o cliente com o cartão final 012 já realizou 88 compras na Cafeteria. O gráfico utilizado para realizar a análise foi o **Gráfico de barras empilhadas**. Com base na análise de recorrência de clientes, a loja pode criar programas de fidelidade ou recompensas personalizadas para clientes frequentes, como o cliente com o cartão final 012, incentivando ainda mais sua lealdade e aumentando o ticket médio.

![](https://i.postimg.cc/s2BdCXzd/Screenshot-4.jpg)

**Análise de Receita ao Longo do Tempo**: Os meses que mais venderam foram, em ordem decrescente, Maio, Junho e Março com valores de, respectivamente R$ 9,1 mil, R$7,1 mil e R$ 6,9 mil. Com base na análise de receita, a loja pode intensificar campanhas promocionais nos meses de maior venda, como Maio, Junho e Março, replicando as estratégias que foram bem-sucedidas nesses períodos. Além disso, é importante planejar o estoque e a equipe para atender à maior demanda nesses meses e, paralelamente, criar ações específicas para aumentar as vendas nos períodos de menor desempenho.

![](https://i.postimg.cc/rFD85WQW/Screenshot-6.jpg)

**Receita por Dia da semana e Hora**: 
* Os horários de pico de venda são concentrados entre 8h e 10h, com maior receita gerada às 8h (R$ 4,5 mil) e 9h (R$ 5,4 mil). Esses horários coincidem com o café da manhã, mostrando que a loja é mais movimentada nesse período. 
* Aos sábados e domingos as vendas caem em relação aos dias úteis, sugerindo que o público alvo da cafeteria seja composto por estudantes ou trabalhadores, que frequentariam aos dias de semana. O gráfico utilizado para realizar a análise foi o **Matriz**.
*  Com base na análise de receita por dia da semana e hora, a loja pode intensificar promoções e combos de café da manhã entre 8h e 10h para aproveitar os horários de pico. Nos finais de semana, estratégias como ofertas especiais ou eventos podem ser implementadas para atrair mais clientes e equilibrar as vendas com os dias úteis.

![](https://i.postimg.cc/ht8jH2SR/Screenshot-5.jpg)

## KPIs que foram exploradas:

* **Total da receita**: Total de receita gerada no período observado foi de 39.656,78.

* **Quantidade de Vendas**: 1.208 Total de pedidos realizados.

* **Ticket médio**: Ticket médio das vendas é de 32,83. 

* **Produto com maior rotatividade**: Produto que foi campeão de vendas no cardápio foi o Latte.

* **Receita por produto**: Com a análise correta dos dados, é possível identificar quais produtos são os mais vendidos. Com essa informação, a empresa pode aplicar estratégias de marketing direcionadas, como promoções e campanhas específicas, para impulsionar ainda mais as vendas desses itens. 

* **Quantidade de transação por meio de pagamento**: A grande parte das transações foram realizadas por meio de cartão (92,63%) e a outra parte com apenas 7,37%. 

* **Quantidade de transação por cliente**: Demonstra a frequência de um cliente com total de transações, meio de pagamento, pedido e horário.

* **Clientes não recorrentes**: O dashboard mostra uma lista de 89 clientes não recorrentes, transmitindo um alto número de clientes não fidelizados, que podem assim chamar a atenção de estratégias de fidelização. 

 

