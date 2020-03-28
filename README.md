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

**file:** *covid-19-ES-CCAA-DatosCasos.csv*

**file:** *covid-19-ES-CCAA-DatosCasos.json*


| nombre clave               | Descripcion                | Description                   | data source                                                                                                                                                                                 |
| -------------------------- | -------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `fecha`                    | fecha informe              | report date                   | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)                                                                                                                                          |
| `codigo_pais`              | codigo GeoId               | country name                  | [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements)                                                                                    |
| `nombre_pais`              | nombre del pais            | country name                  |                                                                                                                                                                                             |
| `codigo_iso_ccaa`          | Codigo INE de la CCAA      | Autonomous Community ISO Code | [ISO_3166-2:ES](https://es.wikipedia.org/wiki/ISO_3166-2:ES)                                                                                                                                |
| `codigo_ine_ccaa`          | Codigo INE de la CCAA      | Autonomous Community INE Code | [INE](https://www.ine.es/daco/daco42/codmun/cod_ccaa.htm)                                                                                                                                   |
| `nombre_ccaa`              | Nombre de la CCAA          | Autonomous Community Name     |                                                                                                                                                                                             |
| `casos_confirmados`        | Infectados acumulado       | Infected cumulative           | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm), [dsn.gob.es](https://www.dsn.gob.es/gl/current-affairs/press-room) |
| `casos_hospitalizados`     | hospitalizados acumulativo | hospitalized cumulative       | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm)                                                                     |
| `casos_UCI`                | pacientes en UCI acumulado | Intensive Care cumulative     | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm)                                                                     |
| `casos_fallecidos`         | Defunciones acumulado      | Deaths cumulative             | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm), [dsn.gob.es](https://www.dsn.gob.es/gl/current-affairs/press-room) |
| `casos_recuperados`        | Recuperados acumulado      | Recovered cumulative          | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm)                                                                     |
| `casos_confirmados_diario` | Nuevos casos infectados    | New infected                  | (1)                                                                                                                                                                                         |
| `casos_UCI_diario`         | Nuevos casos UCI           | New intensive care            | (2)                                                                                                                                                                                         |
| `casos_fallecidos_diario`  | Nuevos fallecidos diario   | New deaths                    | (3)                                                                                                                                                                                         |



1. new infected cases are calculated. The formula used is:
  *casos_confirmados(t) - casos_confirmados (t-1)*

2. new intensive cases are calculated. The formula used is:
 *casos_UCI (t) - casos_UCI(t-1)*

3. new death cases are calculated. The formula used is:
*casos_fallecido (t) - casos_fallecido(t-1)*

*Relevant Info* about the data published by the Ministry

`casos_UCI`is a subset of `casos_hospitalizados`

`casos_confirmados`is not the result of adding `casos_hospitalizados` ,`casos_fallecidos`  and `casos_recuperados`. These stauses are not mutually exclusive




------




#### CapacidadHospitalaria

**file:** *covid-19-ES-CCAA-CapacidadHospitalaria.csv*

**file:** *covid-19-ES-CCAA-CapacidadHospitalaria.json*

| nombre clave          | Descripcion                  | Description                                 | Source                                                    |
| --------------------- | ---------------------------- | ------------------------------------------- | --------------------------------------------------------- |
| `nombre_pais`         | nombre del pais              | country name                                |                                                           |
| `codigo_pais`         | codigo GeoId                 | country ID                                  | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)        |
| `nombre_ccaa`         | Nombre de la CCAA            | Autonomous Community Name                   |                                                           |
| `codigo ccaa`         | Codigo INE de la CCAA        | Autonomous Community Code                   | [INE](https://www.ine.es/daco/daco42/codmun/cod_ccaa.htm) |
| `numero_hospitales`   | Hospitales por CCAA          | Number of hospitals by Autonomous Community | mscbs.gob.es                                              |
| `camas_hospitalarias` | Camas hospitalarias por CCAA | Number of hospital beds                     | mscbs.gob.es                                              |
| `camas_agregadas`     | camas añadidas al sistema    | Aditional hospital beds added               | [N/A]]                                                    |

> The parameter camas_agregadas is a placeholder for the extra capacity being added to the system - hotels, campaign hospitals,...

Same resources in different output form

[Webpage with the latest Data](https://docs.google.com/spreadsheets/d/e/2PACX-1vTagwbioq624b3MaX3Je7Ip9rSvlE-P_N2Wja5iGTqHS4m-RUhqu3_N_4ma1hZzmyphI12jt0zub6GV/pubhtml?gid=1915535336&single=true)

[Google Sheets endpoint](https://spreadsheets.google.com/feeds/cells/1YwtJIYgwhmrriCdfyEBRCGrApFFFBEldSlCvbdBGwXg/3/public/full?alt=json)

------

## Data by Ministry of Health (datos-ministerio-salud)

We have added al the reports we have retreived form the official website of the Spanish Health Ministry. These files have different naming structures and the data presented is not homogeneus. 

The whole set of URLs from which reports were downloaded can be found [here](https://docs.google.com/spreadsheets/d/e/2PACX-1vSlbs4xBmZPfaLU-97Eg25uqXsPTX7ievBYajNbK32TlaxyhzQPemXFFYyF-rMkD4kkGcoNl7UQHt7I/pubhtml?gid=0&single=true).


------


## License

All the data can be donloaded and used for free. It would be nice if you just mention us, and spread the word. 

# Contact Us

You can contact us at coronavirus@secuoyas.com