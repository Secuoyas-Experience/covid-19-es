<a href="https://coronavirus.secuoyas.com"><img src="https://coronavirus.secuoyas.com/img/COVID-19-ES-Cover.png" title="covid-19-es-cover" alt="Secuoyas"></a>

# COVID-19-ES-DATA

This repo is intended to extend the resources publicly provided by the Spanish Health Ministry.

Reports are published at [Ministry of Health](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm). However, reports are hard to retrieve, and data is hardcoded.

As a result, we have digitized and organized reports and data, in order to make analysis by third parties easier and faster, as we believe that speed is paramount. 

> This project is a WIP. Structure might change over time.

## Repository Structure

```
COVID-19-ES-DATA
|
|- datos-ccaa-csv
|- datos-ccaa-json
|- datos-ministerio-salud
```

### Data by Autonomous Community (datos-CCAA)

File Naming Convention: covid-19-Country-RegionalDivision-Category

+ Country: GeoId - ES for Spain
+ Regional Division - CCAA for Autonomous Comunity
+ Category



### Data Structure

| nombre clave | Descripcion| Description|
| --- | --- | --- |
| fecha | fecha informe | report date |
| nombre_pais | nombre del pais | country name |
| codigo_pais | codigo GeoId | country name |
| nombre_ccaa | Nombre ce la CCAA | Autonomous Comunity Name |
| casos_confirmados | infectados acumulado | infected cumulative |
| casos_UCI | pacientes en UCI acumulado | Intensive Care cumulative|
| casos_fallecidos | Defunciones acumulado | Deaths cumulative|
| casos_recuperados | Recuperados acumulado | Recovered cumulative |
| casos_confirmado_diario | nuevos casos infectados | new infected |

** new infected are calculated: total amount of infected - Total maount of infected previous day **

+ Subject - Acumulado for cumulative

### Data by Ministry of Health (datos-ministerio-salud)

We have added al the reports we have downloaded form the official website. these files have different naming structures and the data presented is not hoogeneus. 

The whole set of URLs from which reports were downloaded can be found [here](https://docs.google.com/spreadsheets/d/1lZNB6Hcdq9cbaZCZKvloJfdzicLzvdH6-1jGIL6uE5E/edit?usp=sharing).


