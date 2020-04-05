<a href="https://coronavirus.secuoyas.com"><img src="https://coronavirus.secuoyas.com/img/COVID-19-ES-Cover.png" title="covid-19-es-cover" alt="Secuoyas"></a>

# COVID-19-ES-DATA

This repo is intended to extend the resources publicly provided by the Spanish Health Ministry and other Regional Health Agencies in Spain.

We have put together 7 datasets for the different Autonomous Communinites in Spain at different administrative  levels:

### At the Autonomous Autonomy Level (CCAA)- 3 Datasets

*CCAA-SerieHistorica* - Aggregated by and downloaded from mscbs.gob.es
*CCAA-DatosCasos* - previous dataset, Enriched with IDs and GeoData by Autonomous Autonomy, plus daily changes (calculated)
*CCAA-CapacidadHospitalaria* - Data retieved and digitized from mscbs.gob.es 

### At the Regional Level (Provincias)- 4 Datasets
*ES-AN-DatosCasos* - Provinces of Andalucía - Agregated by [juntadeandalucia.es](https://www.juntadeandalucia.es/organismos/saludyfamilias/areas/salud-vida/paginas/Nuevo_Coronavirus.html)
*ES-CL-DatosCasos* - Provinces of Catilla y León - Aggrgated by [jcyl.es](https://analisis.datosabiertos.jcyl.es/pages/coronavirus/situacin-actual#descarga-de-datasets)
*ES-CM-DatosCasos* - Provinces of Catilla La Mancha - Aggrgated by [sanidad.castillalamancha.es](https://sanidad.castillalamancha.es/notas-de-prensa)
*ES-CV-DatosCasos* - Provinces of Comunidad Valenciana - Aggrgated by [gva.es](https://www.gva.es)


## Disclaimer
Unfortunately reports are hard to retrieve, and data is usually hardcoded in prss notes. This isse becomes the raison-d'etre of this project.

We have digitized and organized reports and data, in order to make analysis by third parties easier and faster, as we believe that speed is paramount. 

There might be some differences between the reported data and the dataset we have assembled. We have been correcting issues when wsa factual mistakes in the reporting. Unfortunatelly, We gouldn´t fill all the gaps.



> This project is a WIP. Structure might change over time.

----

## Repository Structure

The repo is structured by the format supporting the data.

```
COVID-19-ES-DATA
|
|- datos-ccaa-csv
|- datos-ccaa-json
|- informes-ministerio-salud
|- informes-ISCIII
|- informesMoMo
```

## File Name Structure

File Naming Convention: covid-19-Country-RegionalDivision-Category

+ Country: GeoId - ES for Spain
+ Regional Division - ISO 3166-1 alpha-2
+ Category


### Regional divisions

Aggregated  at the Autonomous Comunity Level: CCAA `$codigo_iso_ccaa`
 

| CCAA                 | nombreCcaa           | codigoIsoCcaa |
| -------------------- | -------------------- | ------------- |
| Andalucía            | Andalucía            | ES-AN         |
| Aragón               | Aragón               | ES-AR         |
| Asturias             | Asturias             | ES-AS         |
| Illes Balears        | Baleares             | ES-IB         |
| Canarias             | Canarias             | ES-CN         |
| Catabria             | Cantabria            | ES-CN         |
| Castilla - La Mancha | Castilla-La Mancha   | ES-CM         |
| Castilla y León      | Castilla y León      | ES-CL         |
| Catalunya            | Cataluña             | ES-CT         |
| Ceuta                | Ceuta                | ES-CE         |
| Comunitat Valenciana | Comunidad Valenciana | ES-CT         |
| Extremadura          | Extremadura          | ES-EX         |
| Galicia              | Galicia              | ES-GA         |
| Comunidad de Madrid  | Madrid               | ES-MA         |
| Melilla              | Melilla              | ES-ML         |
| Murcia, Region de    | Murcia               | ES-MC         |
| Nafaroa              | Navarra              | ES-NC         |
| Euskadi              | Pais Vasco           | ES-PV         |
| La Rioja             | La Rioja             | ES-RI         |


Aggegated at the Province level 

> Table to be created. Visit [The API page of coronavirus.secuoyas.com](https://coronavirus.secuoyas.com/coronavirus-api.html) for a complete table.


## Data Structure

### At the autonomous comuity level (CCAA)

**file:** *covid-19-ES-CCAA-DatosCasos.csv*



| nombre clave             | Descripcion                | Description                   | data source                                                                                                                                                                                 |
| ------------------------ | -------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `fecha`                  | fecha informe              | report date                   | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)                                                                                                                                          |
| `codigoIso_Pais`         | codigo GeoId / ISO         | country name                  | [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements)                                                                                    |
| `nombrePais`             | nombre del pais            | country name                  |                                                                                                                                                                                             |
| `codigoIso_Ccaa`         | Codigo INE de la CCAA      | Autonomous Community ISO Code | [ISO_3166-2:ES](https://es.wikipedia.org/wiki/ISO_3166-2:ES)                                                                                                                                |
| `codigoIneCcaa`          | Codigo INE de la CCAA      | Autonomous Community INE Code | [INE](https://www.ine.es/daco/daco42/codmun/cod_ccaa.htm)                                                                                                                                   |
| `nombreCcaa`             | Nombre de la CCAA          | Autonomous Community Name     |                                                                                                                                                                                             |
| `casosConfirmados`       | Infectados acumulado       | Infected cumulative           | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm), [dsn.gob.es](https://www.dsn.gob.es/gl/current-affairs/press-room) |
| `casosHospitalizados`    | hospitalizados acumulativo | hospitalized cumulative       | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm)                                                                     |
| `casosUCI`               | pacientes en UCI acumulado | Intensive Care cumulative     | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm)                                                                     |
| `casosFallecidos`        | Defunciones acumulado      | Deaths cumulative             | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm), [dsn.gob.es](https://www.dsn.gob.es/gl/current-affairs/press-room) |
| `casosRecuperados`       | Recuperados acumulado      | Recovered cumulative          | [mscbs.gob.es](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm)                                                                     |
| `casosConfirmadosDiario` | Nuevos casos infectados    | New infected                  | (1)                                                                                                                                                                                         |
| `casosUCIDiario`         | Nuevos casos UCI           | New intensive care            | (2)                                                                                                                                                                                         |
| `casosFallecidosDiario`  | Nuevos fallecidos diario   | New deaths                    | (3)                                                                                                                                                                                         |


#### Notes

1. new infected cases are calculated. The formula used is:
  *casos_confirmados(t) - casos_confirmados (t-1)*

2. new intensive cases are calculated. The formula used is:
 *casos_UCI (t) - casos_UCI(t-1)*

3. new death cases are calculated. The formula used is:
*casos_fallecido (t) - casos_fallecido(t-1)*

*Relevant Info* about the data published by the Ministry

`casosUCI`is a subset of `casosHospitalizados`

`casosConfirmados`is not the result of adding `casosHospitalizados` ,`casosFallecidos`  and `casosRecuperados`. These stauses are not mutually exclusive

### At the Regional Level (Provincias)

**file:** *covid-19-ES-AN-DatosCasos.csv*
**file** *covid-19-ES-CL-DatosCasos.csv*
**file** *covid-19-ES-CM-DatosCasos.csv*
**file** *covid-19-ES-CV-DatosCasos.csv*

> **DOCUMENTATION IN PROGRESS**
> Structure to be documented, but it is quite similar to the previous one.


------




#### CapacidadHospitalaria

**file:** *covid-19-ES-CCAA-CapacidadHospitalaria.csv*

**file:** *covid-19-ES-CCAA-CapacidadHospitalaria.json*

| nombre clave         | Descripcion                  | Description                                 | Source                                                                                                       |
| -------------------- | ---------------------------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| `nombrePais`         | nombre del pais              | country name                                |                                                                                                              |
| `codigoPais`         | codigo GeoId                 | country ID                                  | [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)                                                           |
| `nombreCcaa`         | Nombre de la CCAA            | Autonomous Community Name                   |                                                                                                              |
| `codigoCcaa`         | Codigo INE de la CCAA        | Autonomous Community Code                   | [INE](https://www.ine.es/daco/daco42/codmun/cod_ccaa.htm)                                                    |
| `numeroHospitales`   | Hospitales por CCAA          | Number of hospitals by Autonomous Community | [mscbs.gob.es](https://www.mscbs.gob.es/ciudadanos/prestaciones/centrosServiciosSNS/hospitales/home.htm) (1) |
| `camasHospitalarias` | Camas hospitalarias por CCAA | Number of hospital beds                     | mscbs.gob.es                                                                                                 |
| `camasAgregadas`     | camas añadidas al sistema    | Aditional hospital beds added               | [N/A](2)                                                                                                     |

> (1) Data updated by source on 13/12/2018
> (2)The parameter camas_agregadas is a placeholder for the extra capacity being added to the system - hotels, campaign hospitals,...

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