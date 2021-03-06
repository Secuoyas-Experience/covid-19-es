# Changelog

## 2020-04-25

### Adds dataset: ES-AS
Add data from all the regional subdivisions of Asturias - Provincias
Digitized all the data exposed in the [news reports](https://app.transparenciaendatos.es/v/#!/5e8dee9d26e3017b3da65ba8)

| iso_code | Provincia |
| -------- | --------- |
| ES-O     | Asturias  |


## 2020-04-24

### Adds dataset: ES-CB
Add data from all the regional subdivisions of Cantabria - Provincias
Digitized all the data exposed in the [news reports](https://www.cantabria.es/web/comunicados)

| iso_code | Provincia |
| -------- | --------- |
| ES-S     | Santander |


## 2020-04-11

## Improves ES-AR dataset
Added new data for first days of the outbreak

## Fixes some bugs
A couple of days have been fixed in the ES-AN and ES-AR datasets.
We have improved the QA process to avoid these mistakes in the future.


## 2020-04-09

### Adds dataset: ES-EX
Add data from all the regional subdivisions of Extremadura - Provincias
Digitized all the data exposed in the [news reports](http://www.juntaex.es/comunicacion/hemeroteca)

| iso_code | Provincia |
| -------- | --------- |
| ES-BA    | Badajoz   |
| ES-CC    | Cáceres   |
 
### added new parameter: *casosHospitalizadosDiario*
Although the calculation was trivial form the data, we realized that it was more consistent with the data scructure adding this to the tables.

### Bug Fixing
We fixed a mistake in the deployment script for the dataset of Aragón. We were pushing the Google urls instead of the data :facepalm:
Sorry about that!

## 2020-04-07

### Update the naming convention for the parameters
Change notation to camelCase: Switch format form underscores, as in `name_description`to camelCase as in `nameDescription` to comply with json standards.

### Improve ES-CM dataset

Calculated casosHospitalizados from a detailed list provided by hospitals and aggregated by Provincia.




## 2020-04-06
Adds dataset: ES-AR
Add data from all the regional subdivisions of Aragón - Provincias
Digitized all the data exposed in the [news reports](http://www.aragonhoy.net/index.php/mod.noticias/mem.listadoArea/area.1050/relmenu.9/regini.60)

| iso_code | Provincia |
| -------- | --------- |
| ES-HU    | Huesca    |
| ES-TE    | Teruel    |
| ES-Z     | Zaragoza  |

## 2020-04-05
Adds dataset: ES-CV
Add data from all the regional subdivisions of Comunidad Valenciana - Provincias
Digitized all the data exposed in the [news reports](https://www.gva.es/va/inicio/area_de_prensa/ap_notas_prensa?tipoContenido=26&zona=21&botonBuscar=buscar&busquedaorganismo=3.07)

| iso_code | Provincia |
| -------- | --------- |
| ES-A     | Alicante  |
| ES-CS    | Castellón |
| ES-V     | Valencia  |


## 2020-04-02
Adds dataset: ES-CM
Add data from all the regional subdivisions of Castilla La Mancha - Provincias
Digitized all the data exposed in the [news reports](https://sanidad.castillalamancha.es/notas-de-prensa)


> Warning: casos_confirmados of 2020-03-23 and 2020-03-24 are incremental. Data from 2020-03-22 is lacking.


| iso_code | Provincia   |
| -------- | ----------- |
| ES-AB    | Albacete    |
| ES-CR    | Ciudad Real |
| ES-CU    | Cuenca      |
| ES-GU    | Guadalajara |
| ES-TO    | Toledo      |



## 2020-04-02

Adds reports for the folders:

* Informes-MoMo
* Informes-ISCIII


## 2020-03-30

### Add Regional data for Castilla Y León (ES-CL)

Normalized all the data exposed in the [datasets exposed](https://analisis.datosabiertos.jcyl.es/pages/coronavirus/situacin-actual#descarga-de-datasets)
Extract and arrange data form all the regional subdivisions of CyL - Provincias to match the other data models of this dataset

| iso_code | Provincia  |
| -------- | ---------- |
| ES-AV    | Ávila      |
| ES-BU    | Burgos     |
| ES-LE    | León       |
| ES-P     | Palencia   |
| ES-SA    | Salamanca  |
| ES-SG    | Segovia    |
| ES-SO    | Soria      |
| ES-VA    | Valladolid |
| ES-ZA    | Zamora     |


## 2020-03-29

### Add Regional data for Andalucía (ES-AL)

Digitized all the data exposed in the [news reports](https://www.juntadeandalucia.es/organismos/saludyfamilias/areas/salud-vida/paginas/coronavirus-comunicados-anteriores.html)
Add data from all the regional subdivisions of Andalucía - Provincias

| iso_code | Provincia |
| -------- | --------- |
| ES-AL    | Almería   |
| ES-CA    | Cádiz     |
| ES-CO    | Córdoba   |
| ES-GR    | Granada   |
| ES-H     | Huelva    |
| ES-J     | Jaén      |
| ES-MA    | Málaga    |
| ES-SE    | Sevilla   |
----

## 2020-03-16

### Repo Started

Added information form the [Ministry of Health](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm) - Ministerio de Sanidad