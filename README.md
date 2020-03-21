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

## Data by Autonomous Community (datos-CCAA)

File Naming Convention: covid-19-Country-RegionalDivision-Category

+ Country: GeoId - ES for Spain
+ Regional Division - CCAA for Autonomous Comunity
+ Category



## Data Structure

#### DatosCasos

**file:** *covid-19-ES-CCAA-DatosCasos.json*

| nombre clave             | Descripcion                | Description               |
| ------------------------ | -------------------------- | ------------------------- |
| fecha                    | fecha informe              | report date               |
| nombre_pais              | nombre del pais            | country name              |
| codigo_pais              | codigo GeoId               | country name              |
| nombre_ccaa              | Nombre de la CCAA          | Autonomous Community Name |
| codigo_ccaa              | Codigo INE de la CCAA      | Autonomous Community Code |
| casos_confirmados        | infectados acumulado       | infected cumulative       |
| casos_hospitalizados     | hospitalizados acumulativo | hospitalized cumulative   |
| casos_UCI                | pacientes en UCI acumulado | Intensive Care cumulative |
| casos_fallecidos         | Defunciones acumulado      | Deaths cumulative         |
| casos_recuperados        | Recuperados acumulado      | Recovered cumulative      |
| casos_confirmados_diario | Nuevos casos infectados    | New infected              |
| casos_UCI_diarios        | Nuevos casos UCI           | New intensive care        |
| casos_fallecidos_diario  | Nuevos fallecidos diario   | New deaths                |



new infected cases are calculated. The formula used is:
*Total amount of infected (t) - Total amount of infected (t-1)*

new intensive case cases are calculated. The formula used is:
 *casos_UCI (t) - casos_UCI(t-1)*

new intensive case cases are calculated. The formula used is:
*casos_fallecido (t) - casos_fallecido(t-1)*

#### CapacidadHospitalaria

**file:** *covid-19-ES-CCAA-CapacidadHospitalaria.json*

| nombre clave        | Descripcion                  | Description                                 |
| ------------------- | ---------------------------- | ------------------------------------------- |
| nombre_pais         | nombre del pais              | country name                                |
| codigo_pais         | codigo GeoId                 | country name                                |
| nombre_ccaa         | Nombre de la CCAA            | Autonomous Community Name                   |
| codigo ccaa         | Codigo INE de la CCAA        | Autonomous Community Code                   |
| numero_hospitales   | Hospitales por CCAA          | number of hospitals by Autonomous Community |
| camas_hospitalarias | camas hospitalarias por CCAA | number of hospital beds                     |
| camas_agregadas     | camas añadidas al sistema    | aditional hospital beds added               |

> The parameter camas_agregadas is a placeholder for the extra capacity being generated into the system - hotels, campaign hospitals,...


[Webpage with the latest Data](https://docs.google.com/spreadsheets/d/e/2PACX-1vTagwbioq624b3MaX3Je7Ip9rSvlE-P_N2Wja5iGTqHS4m-RUhqu3_N_4ma1hZzmyphI12jt0zub6GV/pubhtml?gid=1915535336&single=true)
[Google Sheets endpoint](https://spreadsheets.google.com/feeds/cells/1YwtJIYgwhmrriCdfyEBRCGrApFFFBEldSlCvbdBGwXg/3/public/full?alt=json)

## Data by Ministry of Health (datos-ministerio-salud)

We have added al the reports we have downloaded form the official website. these files have different naming structures and the data presented is not hoogeneus. 

The whole set of URLs from which reports were downloaded can be found [here](https://docs.google.com/spreadsheets/d/1lZNB6Hcdq9cbaZCZKvloJfdzicLzvdH6-1jGIL6uE5E/edit?usp=sharing).

