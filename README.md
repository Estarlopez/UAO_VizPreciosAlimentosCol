# Análisis para la visualización de precios de los alimentos básicos en los principales mercados en Colombia en el tiempo.

Implementación de un análisis de datos para visualizar la evolución de precios básicos en los principales mercados de colombia durante 25 años, desde el 2024 hacia atrás


Diccionario de datos:

## Diccionario de Variables

| Variable       | Tipo de Dato                         | Descripción                                                                                                                                 | Unidad de Medida                    |
|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| date          | Fecha (date / object)                | Fecha de registro del precio. Formato YYYY-MM-DD. El día siempre es 15 (punto medio del mes como referencia de recolección mensual).     | Fecha (YYYY-MM-DD)                  |
| admin1        | Categórica (nominal)                 | Departamento de Colombia donde se ubica el mercado. Corresponde al primer nivel administrativo del país.                                  | Texto (nombre departamento)         |
| admin2        | Categórica (nominal)                 | Municipio o distrito donde se ubica el mercado. Segundo nivel administrativo.                                                              | Texto (nombre municipio)            |
| market        | Categórica (nominal)                 | Nombre del mercado donde se registra el precio. Corresponde a centros de abastos o plazas mayoristas de las principales ciudades.        | Texto (nombre mercado)              |
| market_id     | Numérica (discreta / ID)             | Identificador numérico único del mercado en el sistema WFP.                                                                                | ID numérico                         |
| latitude      | Numérica (continua)                  | Latitud geográfica del mercado en grados decimales.                                                                                        | Grados decimales                    |
| longitude     | Numérica (continua)                  | Longitud geográfica del mercado en grados decimales.                                                                                       | Grados decimales                    |
| category      | Categórica (nominal)                 | Categoría alimentaria del producto según clasificación WFP: cereals and tubers, meat/fish/eggs, milk/dairy, vegetables/fruits, pulses/nuts, oil/fats, miscellaneous food, non-food. | Texto (categoría)                   |
| commodity     | Categórica (nominal)                 | Nombre específico del producto alimentario o no alimentario registrado.                                                                   | Texto (nombre producto)             |
| commodity_id  | Numérica (discreta / ID)             | Identificador numérico único del producto en el sistema WFP.                                                                               | ID numérico                         |
| unit          | Categórica (nominal)                 | Unidad de medida en la que se registra el precio del producto.                                                                             | Texto (unidad)                      |
| priceflag     | Categórica (nominal)                 | Indicador del tipo de dato de precio: actual (precio observado directamente), aggregate (promedio calculado), actual,aggregate (combinación). | Texto (flag)                        |
| pricetype     | Categórica (binaria)                 | Tipo de precio según el nivel de la cadena de distribución: Wholesale (mayorista) o Retail (minorista).                                   | Texto (tipo precio)                 |
| currency      | Categórica (constante)               | Moneda en la que se registra el precio. Todos los registros están en pesos colombianos.                                                   | Código ISO moneda                   |
| price         | Numérica (continua)                  | Precio del producto en pesos colombianos (COP) por unidad de medida. Variable central del análisis.                                       | COP (pesos colombianos)             |
| usdprice      | Numérica (continua)                  | Precio equivalente en dólares estadounidenses (USD), calculado con la tasa de cambio del momento del registro.                            | USD (dólares)                       |
