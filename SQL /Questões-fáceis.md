
   # Questões fáceis de SQL 
 ## Segue uma lista selecionada de questões fáceis de SQL retiradas diretamente do site HackerRank.

## 1 - Select All
Consulte todas as colunas (atributos) para cada linha na tabela CITY. 
 A tabela CITY é descrita da seguinte forma: 
 
![image](https://github.com/user-attachments/assets/951472ee-3f83-44de-8d3e-ed018beb3137)

##### Resposta: 
```SELECT * FROM city```

## 2 - Japanese Cities' Attributes
Consulte todos os atributos de cada cidade japonesa na tabela CITY. O COUNTRYCODE para o Japão é JPN.
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/4bd8692a-fe60-45e7-84ce-4eb187eddf96)

##### Resposta:

```
   SELECT *
   FROM CITY
   WHERE COUNTRYCODE = 'JPN'
   ```

## 3 - Japanese Cities' Names
Consulte os nomes de todas as cidades japonesas na tabela CITY. O COUNTRYCODE para o Japão é JPN.
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/69c009d8-f31f-41dc-936f-975000506f5f)

##### Resposta:
```
SELECT NAME 
FROM CITY 
WHERE COUNTRYCODE = 'JPN'
```

## 4 - Select By ID
Consultar todas as colunas de uma cidade em CITY com o ID 1661.
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/49fa4eee-f43a-4b34-a7bf-1186397ed29c)

##### Resposta:
```
SELECT *
FROM CITY
WHERE ID = 1661
```
## 5 - Revising the Select Query I
Consulte todas as colunas de todas as cidades americanas na tabela CITY com populações maiores que 100.000. O CountryCode para América é EUA.
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/7d87b1a4-42fc-4e7a-8903-80ef4db1fc50)

##### Resposta:
```
SELECT *
FROM CITY 
WHERE COUNTRYCODE = 'USA'
  AND POPULATION > 100000 
```
## 6 - Revising the Select Query II
Consulte o campo NAME para todas as cidades americanas na tabela CITY com populações maiores que 120.000. O CountryCode para América é EUA.
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/a4366c08-6069-414c-8577-7e255777b897)

##### Resposta:
```
SELECT NAME
FROM CITY 
WHERE POPULATION > 120000
AND COUNTRYCODE = 'USA'
```

## 7 - Weather Observation Station 1
Consulte uma lista de CIDADE e ESTADO da tabela ESTAÇÃO.
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/12abeae4-8a96-49e3-be1e-0931f595fd16)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT CITY, STATE 
FROM STATION 
```
## 8 - Weather Observation Station 2
Consulte os dois valores a seguir na tabela STATION:
A soma de todos os valores em LAT_N arredondada para uma escala de 2 casas decimais.
A soma de todos os valores em LONG_W arredondada para uma escala de 2 casas decimais.
Input Format
A tabela STATION é descrita da seguinte forma:
![image](https://github.com/user-attachments/assets/ef388eb2-20f3-4690-b861-85931ffe5dae)
onde LAT_N é a latitude norte e LONG_W é a longitude oeste.
Output Format
Seus resultados devem estar no formato:
lat lon
Onde lat é a soma de todos os valores em LAT_N e é a soma de todos os valores em LONG_W. Ambos os resultados devem ser arredondados para uma escala de 2 casas decimais.

##### Resposta:
```
SELECT ROUND (SUM(LAT_N), 2) , ROUND(SUM(LONG_W), 2) 
FROM STATION
```

## 9 - Weather Observation Station 3
Consulte uma lista de nomes de CIDADES de ESTAÇÃO para cidades que tenham um número de identificação par. Exiba os resultados em qualquer ordem, mas exclua duplicatas da resposta.
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/4510ccb1-6097-4284-8a75-dd0c593e1e8e)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT DISTINCT CITY
FROM STATION 
WHERE ID % 2 = 0;
```
## 10 - Weather Observation Station 4 
Encontre a diferença entre o número total de entradas CITY na tabela e o número de entradas CITY distintas na tabela.
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/6ed735f1-7509-4b55-95c1-2dde1ffad7d4)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

Por exemplo, se houver três registros na tabela com os valores CITY 'New York', 'New York', 'Bengalaru', haverá 2 nomes de cidades diferentes: 'New York' e 'Bengalaru'. A consulta retorna , porque número total de registros - número de nomes de cidades exclusivos = 3 - 2 = 1.

##### Resposta:
```
SELECT
COUNT (CITY) - COUNT (DISTINCT CITY)
FROM STATION;
```
## 11 - Weather Observation Station 6
Consulte a lista de nomes de CIDADES que começam com vogais (por exemplo, a, e, i, o ou u) em STATION. Seu resultado não pode conter duplicatas.
 Input Format
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/11592738-098a-4ea8-a1d6-5b5613e37108)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT CITY
FROM STATION 
WHERE LEFT (CITY, 1) IN ('A', 'E', 'I', 'O', 'U')
```
## 12 - Weather Observation Station 7
Consulte a lista de nomes de CIDADES terminados em vogais (a, e, i, o, u) da ESTAÇÃO. Seu resultado não pode conter duplicatas.
Input Format
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/171a1fef-36ca-4530-a86e-78b96415beaf)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT DISTINCT CITY
FROM STATION
WHERE RIGHT (CITY, 1) IN ('A', 'E', 'I', 'O', 'U');
```
## 13 - Weather Observation Station 8
Consulte a lista de nomes de CIDADES de ESTAÇÃO que possuem vogais (por exemplo, a, e, i, o e u) como primeiro e último caracteres. Seu resultado não pode conter duplicatas.
Input Format
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/222c3e79-bf0d-4c31-a114-cd8a271d2ec2)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT DISTINCT CITY
FROM STATION
WHERE LEFT(CITY, 1) IN ('A', 'E', 'I', 'O', 'U')
AND RIGHT(CITY, 1) IN ('A', 'E', 'I', 'O', 'U');
```
## 14 - Weather Observation Station 9
Consulte a lista de nomes de CIDADES de ESTAÇÃO que não começam com vogais. Seu resultado não pode conter duplicatas.
Input Format
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/1bcf570d-99de-4cf4-99d2-3c2aa283ad5a)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT LEFT(CITY, 1) IN ('A', 'E', 'I', 'O', 'U');
```
## 15 - Weather Observation Station 10
Consulte a lista de nomes de CIDADES da ESTAÇÃO que não terminam com vogais. Seu resultado não pode conter duplicatas.
Input Format
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/fa978753-1df7-4640-9beb-2cf34b0fb41f)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT RIGHT(CITY, 1) IN ('A', 'E', 'I', 'O', 'U');
```

## 16 - Weather Observation Station 11
Consulte a lista de nomes de CIDADES da ESTAÇÃO que não começam com vogais ou não terminam com vogais. Seu resultado não pode conter duplicatas.
Input Format
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/299b4107-6557-4cc1-8218-a341f87199a5)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT DISTINCT CITY
FROM STATION
WHERE NOT LEFT(CITY, 1) IN ('A', 'E', 'I', 'O', 'U')
OR NOT RIGHT(CITY, 1) IN ('A', 'E', 'I', 'O', 'U');
```

## 17 - Weather Observation Station 12
Consulte a lista de nomes de CIDADES da ESTAÇÃO que não começam com vogais e não terminam com vogais. Seu resultado não pode conter duplicatas.
Input Format
A tabela STATION é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/7c6ee490-da0c-41b8-8f84-0243b85980cf)

Onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT DISTINCT CITY
FROM STATION
WHERE LEFT(CITY, 1) NOT IN ('A', 'E', 'I', 'O', 'U')
AND RIGHT(CITY, 1) NOT IN ('A', 'E', 'I', 'O', 'U');
```
## 18 - Weather Observation Station 13 
Consultar a soma das latitudes do norte (LAT_N) da ESTAÇÃO com valores maiores que 38.7880 e menos de 137.2145. Trunque sua resposta para 4 casas decimais.
Input Format
A tabela STATION é descrita da seguinte forma:
![image](https://github.com/user-attachments/assets/e8e9c6bf-1699-4de9-8151-73a4f99154cb)
onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT ROUND (SUM(LAT_N), 4) 
FROM STATION 
WHERE LAT_N > 38.7880 AND LAT_N < 137.2345
```
## 19 - Weather Observation Station 14
Consultar o maior valor das latitudes do norte (LAT_N) da ESTAÇÃO que seja menor que 137.2345. Trunque sua resposta para 4 casas decimais.
Input Format
A tabela STATION é descrita da seguinte forma:
![image](https://github.com/user-attachments/assets/4552dfa3-bd40-4f38-9427-4514d01a50a6)
onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT ROUND (MAX(LAT_N), 4) 
FROM STATION
WHERE LAT_N < 137.2345
```
## 20 - Weather Observation Station 15
Consulte a Longitude Ocidental (LONG_W) para encontrar a maior Latitude Norte (LAT_N) em STATION que seja menor que 137.2345. Arredonde sua resposta para 4 casas decimais.
Input Format
A tabela STATION é descrita da seguinte forma:
![image](https://github.com/user-attachments/assets/79588633-8b87-49ff-97ce-76cf3bb4aaaa)
onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT ROUND (LONG_W, 4) 
FROM STATION 
WHERE LAT_N < 137.2345 
ORDER BY LAT_N 
DESC LIMIT 1;
```
## 21 - Weather Observation Station 16
Consultar a menor latitude norte (LAT_N) da ESTAÇÃO que seja maior que 38.7780. Arredonde sua resposta para 4 casas decimais.
Input Format
A tabela STATION é descrita da seguinte forma:
![image](https://github.com/user-attachments/assets/d9fd75ef-6e01-4b50-817e-47f0773ea7a2)
onde LAT_N é a latitude norte e LONG_W é a longitude oeste.

##### Resposta:
```
SELECT ROUND (LAT_N, 4)
FROM STATION 
WHERE LAT_N  >  38.7780 
ORDER BY LAT_N 
LIMIT 1;
```
## 22 - Weather Observation Station 17
Consulte a Longitude Ocidental (LONG_W) onde a menor Latitude Norte (LAT_N) em STATION é maior que 38.7780. Arredonde sua resposta para 4 casas decimais.
Input Format
A tabela STATION é descrita da seguinte forma:
![image](https://github.com/user-attachments/assets/09668a62-9967-4f7c-bf12-f1b336248e46)
onde LAT_N é a latitude norte e LONG_W é a longitude oeste.
##### Resposta:
```
SELECT ROUND (LONG_W,  4)
FROM STATION 
WHERE LAT_N > 38.7780 
ORDER BY LAT_N ASC 
LIMIT 1;
```

## 19 - Higher Than 75 Marks
Consulte o nome de qualquer aluno em STUDENTS que tenha pontuação superior 75 a pontos. Ordene sua saída pelos três últimos caracteres de cada nome. Se dois ou mais alunos tiverem nomes terminados nos mesmos três últimos caracteres (por exemplo: Bobby, Robby, etc.), ordene-os secundariamente por ID crescente.
Input Format
A tabela STUDENTS é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/aeab6145-bf5c-491b-99db-73461089b3bd)

A coluna Name contém apenas letras maiúsculas (A-Z) e minúsculas (a-z).

Sample Input
![image](https://github.com/user-attachments/assets/a055ee86-b291-4d68-bb36-662b9437866b)

Sample Output
Ashley
Julia
Belvet

Explicação
Somente Ashley, Julia e Velvet têm pontos > 75. Se você olhar para os três últimos caracteres de cada um dos seus nomes, não há duplicatas e 'ley' < 'lia' < 'vet'.

##### Resposta:
```
SELECT Name
FROM STUDENTS
WHERE Marks > 75
ORDER BY RIGHT(Name, 3), ID ASC;
```
## 19 - Employee Names
Escreva uma consulta que imprima uma lista de nomes de funcionários (por exemplo: o atributo name) da tabela Employee em ordem alfabética.
Input Format
A tabela Employee, que contém os dados dos funcionários de uma empresa, é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/26d7b718-06e5-4484-84e7-2279ab42809b)

Onde employee_id é o número de identificação do funcionário, name é o nome dele, months é o número total de meses que ele trabalha na empresa e salary é o salário mensal.

Sample Input
![image](https://github.com/user-attachments/assets/5521950d-6523-4418-a6b6-5d41ff990496)

Sample Output
Angela
Bonnie
Frank
Joe
Kimberly
Lisa
Michael
Patrick
Rose
Todd

##### Resposta:
```
SELECT name
FROM Employee
ORDER BY name ASC
```
## 19 - Employee Salaries
Escreva uma consulta que imprima uma lista de nomes de funcionários (por exemplo: o atributo name) para funcionários com salário superior a US$ 2.000 por mês e que estejam empregados há menos de 10 meses. Classifique o resultado em ordem crescente de employee_id.
Input Format
A tabela Employee contendo dados de funcionários de uma empresa é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/8ab9e71a-f303-4d6a-ba15-37d4c2b9812e)

Onde employee_id é o número de identificação do funcionário, name é o nome dele, months é o número total de meses que ele trabalha na empresa e salary é o salário mensal.

Sample Input
![image](https://github.com/user-attachments/assets/d436daed-efa0-47d4-96de-f6ca483ec7f7)

Sample Output
Angela
Michael
Todd
Joe

Explicação
Angela é funcionária há 1 mês e ganha US$ 3.443 por mês.
Michael é funcionário há 6 meses e ganha US$ 2.017 por mês.
Todd é funcionário há 5 meses e ganha US$ 3.396 por mês.
Joe é funcionário há 9 meses e ganha US$ 3.573 por mês.
Ordenamos nossa saída em ordem crescente de employee_id.

##### Resposta:
```
SELECT name
FROM Employee
WHERE salary > 2000
AND months < 10
ORDER BY employee_id ASC
```
## 20 - Revising Aggregations - The Count Function
Input Format
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/704d00be-9d1a-4aaa-b440-6ba7d16bff0f)

##### Resposta:
```
SELECT COUNT(*)
FROM CITY
WHERE Population > 100000;
```
## 21 - Revising Aggregations - The Sum Function
Consulte a população total de todas as cidades em CITY cujo distrito é Califórnia.
Input Format
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/8fc25c9b-f672-443e-a49e-10f66e7097f1)

##### Resposta:
```
SELECT SUM(POPULATION) AS populacao
FROM CITY
WHERE DISTRICT = 'California';
```
## 22 - Revising Aggregations - Averages
Consulte a população média de todas as cidades em CITY cujo distrito é Califórnia.
Input Format
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/682414c3-8998-45a2-a202-6bc900e107e7)

##### Resposta:
```
SELECT AVG (POPULATION) FROM CITY
WHERE DISTRICT = 'California'
```
## 23 - Average Population
Consulte a população média de todas as cidades em CITY, arredondada para o número inteiro mais próximo.
Input Format
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/a82019a1-b767-463f-b691-e8e9d2c6ca91)

##### Resposta:
```
SELECT FLOOR(AVG(Population)) AS AveragePopulation
FROM CITY;
```
## 24 - Japan Population
Consulte a soma das populações de todas as cidades japonesas em CITY. O COUNTRYCODE para o Japão é JPN.
Input Format
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/685d4dc9-38ae-495c-878a-74708f722f1a)

##### Resposta:
```
SELECT SUM(Population) 
FROM CITY
WHERE COUNTRYCODE = 'JPN'
```
## 25 - Population Density Difference
Consulte a diferença entre as populações máxima e mínima em CITY.
Input Format
A tabela CITY é descrita da seguinte forma:

![image](https://github.com/user-attachments/assets/120f921e-91ae-4933-b5c2-9c128d3f13c4)

##### Resposta:
```
SELECT MAX(population) - MIN(population) AS PopulationDifference
FROM CITY;
```
## 26 - Population Census
Considerando as tabelas CITY e COUNTRY, consulte a soma das populações de todas as cidades cujo CONTINENTE é "Asia".
Observação: CITY.CountryCode e COUNTRY.Code são colunas-chave correspondentes.
Input Format
As tabelas CITY e COUNTRY são descritas da seguinte forma:

![image](https://github.com/user-attachments/assets/8a2a4ea4-1e8e-4b49-a1fd-8f511cbe9051)
![image](https://github.com/user-attachments/assets/82279835-5115-4a3b-898b-d1d4c7fe459d)

##### Resposta:
```
SELECT SUM(CITY.Population) AS TotalPopulation
FROM CITY
JOIN COUNTRY ON CITY.CountryCode = COUNTRY.Code
WHERE COUNTRY.Continent = 'Asia';
```
## 27 - African Cities
Considerando as tabelas CITY e COUNTRY, consulte os nomes de todas as cidades cujo CONTINENT é "África".
Observação: CITY.CountryCode e COUNTRY.Code são colunas-chave correspondentes.
Input Format
As tabelas CITY e COUNTRY são descritas da seguinte forma:
![image](https://github.com/user-attachments/assets/0042ff99-c613-49e2-b219-98d00f9f8188)
![image](https://github.com/user-attachments/assets/5cc80786-5296-41f1-bc68-6beda523adba)

##### Resposta:
```
SELECT CITY.Name
FROM CITY
JOIN COUNTRY ON CITY.CountryCode = COUNTRY.Code
WHERE COUNTRY.Continent = 'Africa';
```
## 28 - Average Population of Each Continent
Considerando as tabelas CITY e COUNTRY, consulte os nomes de todos os continentes (COUNTRY.Continent) e suas respectivas populações médias urbanas (CITY.Population), arredondadas para o número inteiro mais próximo.
Observação: CITY.CountryCode e COUNTRY.Code são colunas-chave correspondentes.
Input Format
As tabelas CITY e COUNTRY são descritas da seguinte forma:
![image](https://github.com/user-attachments/assets/991c0887-0538-4421-94d9-cdb02f6bbd1d)
![image](https://github.com/user-attachments/assets/459300f4-c4da-4462-9080-f54a49f0e17d)

##### Resposta:
```
SELECT COUNTRY.Continent, FLOOR(AVG(CITY.Population)) AS AverageCityPopulation
FROM CITY
JOIN COUNTRY ON CITY.CountryCode = COUNTRY.Code
GROUP BY COUNTRY.Continent;
```
## 29 -









