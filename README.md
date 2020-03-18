# COVID-19-ES-DATA

This repo is intended to extend the resources publicly provided by the Spanish Health Ministry.

Reports are published at [Ministry of Health](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm). However, reports are hard to retrieve, and data is hardcoded.

As a result, we have digitized and organized reports and data, in order to make analysis by third parties easier and faster, as we believe that speed is paramount. 


## Repository Structure

```
COVID-19-ES-DATA
|
|- datos-ccaa-csv
|- datos-ccaa-json
|- datos-ministerio-salud
```

### Data by Autonomous Community (datos-CCAA)

File Naming Convention: Country-RegionalDivision-Category-Subject

+ Country: GeoId - ES for Spain
+ Regional Division - CCAA for Autonomous Comunity
+ Category


| Casos Confirmados | Confirmed Cases |
| --- | --- |
| Defunciones | Deaths |
| UCI | Intensive Care |

+ Subject - Acumulado for cumulative

### Data by Ministry of Health (datos-ministerio-salud)

We have added al the reports we have downloaded form the official website. these files have different naming structures and the data presented is not hoogeneus. 

The whole set of URLs from which reports were downloaded can be found [here](https://docs.google.com/spreadsheets/d/1lZNB6Hcdq9cbaZCZKvloJfdzicLzvdH6-1jGIL6uE5E/edit?usp=sharing).


