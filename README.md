# Script de Limpieza de Datos con Python

## Descripción

Este script está diseñado para procesar y combinar archivos CSV de una carpeta especificada.
Verifica los encabezados de los archivos, filtra los datos y los guarda en un nuevo archivo CSV. El script también ordena los datos por fecha y costo.

***Antecedentes***

Tenemos un cliente que gestiona varias tiendas. Cada una de sus tiendas envía periódicamente sus registros de ventas (“tickets”) en formato CSV, 
donde cada archivo representa las ventas de un día específico. Sin embargo, no siempre es tan sencillo, y a veces olvidan eliminar información innecesaria o redundante de los archivos
que envían. Peor aún, también envían archivos adicionales con otras extensiones y nombres que no tienen nada que ver con los registros de ventas.

***Objetivo***

El objetivo es combinar los registros de ventas (tickets) de cada tienda en un conjunto de datos unificado. Los archivos de tickets tienen el formato AAAA-MM-DD-HH-MM-idcliente.csv. 
(Año-mes-dia-hora-minutos-de cliente). En el nuevo archivo, solo necesitamos guardar las columnas date, product, store y cost, sin incluir el ID del cliente.

***Estructura del Script***

El script se divide en dos partes:

1. Creación de la función para extraer los archivos necesarios.

2. Carga de datos en un DataFrame para su posterior procesamiento y análisis, si es necesario.

***Bibliotecas Utilizadas***

**os**: Para manejar operaciones del sistema de archivos.
**csv**: Para leer y escribir archivos CSV.
**re**: Para trabajar con expresiones regulares y buscar archivos con un patrón específico.
**pandas**: Para manejar y manipular datos en DataFrames.

***Problema Encontrado y Solución***

Durante la creación de este script, me encontré con un problema: 
uno de los tickets tenía una fecha inexistente en febrero, lo que causaba un error.
Sin embargo, este ticket coincidía con nuestro patrón de búsqueda y era necesario agregarlo al archivo combinado.
Para resolver este problema, procesé la fecha como una cadena (str) en lugar de un tipo de dato de fecha, lo que permitió evitar errores y mantener la integridad de los datos.

## [Ejemplo de Código](https://github.com/elena210910/DAta_Cleaning/blob/main/Script_python)
# [Ejemplo Los archivos de tickets antes de Limpieza de Datos](https://github.com/elena210910/DAta_Cleaning/blob/main/Ejemplo%20de%20los%20tickets.png)
