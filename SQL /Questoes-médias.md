 # Questões medianas de SQL 
## Segue uma lista selecionada de questões medianas de SQL retiradas diretamente do site HackerRank.

## 1 - Weather Observation Station 18
Consider P1 (a, b) and P2 (c, d) to be two points on a 2D plane.

 happens to equal the minimum value in Northern Latitude (LAT_N in STATION).
 happens to equal the minimum value in Western Longitude (LONG_W in STATION).
 happens to equal the maximum value in Northern Latitude (LAT_N in STATION).
 happens to equal the maximum value in Western Longitude (LONG_W in STATION).
Query the Manhattan Distance between points P1 and P2 and round it to a scale of 4 decimal places.

Input Format

The STATION table is described as follows:
 
![image](https://i.postimg.cc/PxKBwNSY/imagem-2025-06-16-190640207.png)

where LAT_N is the northern latitude and LONG_W is the western longitude.

##### Resposta: 
```
SELECT ROUND(ABS(MIN(LAT_N) - MAX(LAT_N)) + ABS(MIN(LONG_W) - MAX(LONG_W)), 4)
FROM STATION;

```
## 2 - Weather Observation Station 19

Consider P1 (a, c) and P2 (b, d) to be two points on a 2D plane where (a, b) are the respective minimum and maximum values of Northern Latitude (LAT_N) and (c, d) are the respective minimum and maximum values of Western Longitude (LONG_W) in STATION.

Query the Euclidean Distance between points P1 and P2 and format your answer to display 4 decimal digits.

Input Format

The STATION table is described as follows:

![image](https://github.com/user-attachments/assets/05c1ddb0-6002-48cb-a363-44241458e9b5)

where LAT_N is the northern latitude and LONG_W is the western longitude.

##### Resposta: 
```
SELECT ROUND(  SQRT(
    POWER(MIN(LAT_N) - MAX(LAT_N), 2) + 
    POWER(MIN(LONG_W) - MAX(LONG_W), 2)
  ), 
  4
)
FROM STATION;
```



