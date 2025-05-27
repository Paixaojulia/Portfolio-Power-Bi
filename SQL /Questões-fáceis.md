
  # Questões fáceis de SQL 
 ### Segue uma lista selecionada de questões fáceis de SQL retiradas diretamente do site HackerRank.

## 1 - Select All
Consulte todas as colunas (atributos) para cada linha na tabela CITY. 
 A tabela CITY é descrita da seguinte forma: 
![image](https://github.com/user-attachments/assets/951472ee-3f83-44de-8d3e-ed018beb3137)

##### Resposta: 
SELECT * FROM city

## 2 - Japanese Cities' Attributes
Consulte todos os atributos de cada cidade japonesa na tabela CITY. O COUNTRYCODE para o Japão é JPN.
A tabela CITY é descrita da seguinte forma:
![image](https://github.com/user-attachments/assets/4bd8692a-fe60-45e7-84ce-4eb187eddf96)

##### Resposta:
  SELECT *
  FROM CITY
  WHERE COUNTRYCODE = 'JPN';
