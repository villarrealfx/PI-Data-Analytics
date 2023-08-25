# Data Analytics 
## Proyecto Individual # 2 | Sistema de Recomendación de Películas
## Introducción:
El presente proyecto práctico forma parte del curriculum para la carrera de Ciencia de Datos impartido por **Henry** como parte del trayecto de Labs. El mismo consiste en realizar un análisis sobre el mercado de criptomonedas y evaluar el comportamiento de un mínimo de 10 para entregar una propuesta de posible negocios.

El trabajo se realizó en tres etapas bien definidas y complementarias:

1. Trabajo de ETL **(Extract, Transform, Load)**
    * se realizó la ingesta de datos de una fuente externa API coinGecko, y se sirvio de otra fuente del área un documento en formato .csv
    * Se realizó un trabajo de transformación de los datos para adecuarlos a los requerimientos de este trabajo.
    * Se realizó la carga y creación de archivo de datos para ser consumidos posteriormente en el trabajo de EDA.
2. Trabajo de EDA  **(Exploratory Data Analysis)** a los datos resultantes del procedimiento enunciado en el punto 1
3. Trabajo de Visualización **Data Analytics** Se realizó un Daschboard funcional con herramientas de Inteligencia de Negocios a fin de presentar los datos y el análisis obtenido.


## ETL
La información recolectada se realizó consumiendo el recurso de la API de CoinGecko [aqui CoinGeckoAPI](https://www.coingecko.com/es/api) con las siguientes características:<br>

* **`MarketCap.csv`**: 2059 filas y 3 columnas.
* **`Datos por Criptomonedas`** :
    * se realizo ingesta de datos a través de la API señalada anteriormente los cuales presentaba una estructura común como la siguiente:
        * `prices`, `market_caps` y `total_volumes` la cantidad de registros dependia de la criptomoneda.

* Una vez procesada y transformada la data resultó en:
    * catorce (13) archivos csv correspondiente una para cada criptomoneda selecionada
    * un (01) archivo csv correspondiente a la tabla de hechos que se evaluaría en el EDA


## EDA
### El set de datos
La información una vez procesada se encuentra en un CSV (`crypto_fact_table.csv`) con 24.585 filas y 7 columnas.

Cada registro contiene xx características Las columnas son las siguientes:

1. **date**: Fecha de transacción.
2. **name**: Nombre de la criptomoneda.
3. **prices**: Precio de cierre para el día del activo.
4. **daily_return**: Retorno diario del activo.
5. **market_caps**: Capitalización de mercado del activo.
6. **global_cap**: Capitalización global del mercado de criptomonedas.
7. **market_share**: Porcentaje de la porción del aporte del mercado.

En el EDA se realizó en primera instancia una adecuación de los datos para el proposito de la investigación que se realizó seguidamente, se realizó un análisis de parámetros básicos de estadísticos para finalmente llevar a cabo una profunda evaluación de la data utilizando para ello los KPIs seleccionados.


## 2 URLs

1. [https://github.com/villarrealfx/PI-Data-Analytics/tree/main](https://github.com/villarrealfx/PI-Data-Analytics/tree/main)

## Análisis y Resultados:

Para este trabajo se seleccionaron trece (13) criptomonedas bajo el criterio de dejar abierta la posibilidad de inverción en tres áreas bien definidas que son :

Crypto: `Binancecoin` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Dogecoin` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Ethereum` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Litecoin` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Bitcoin` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Ripple` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Tether` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Tron` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Cardano` | Datos Observados en el período desde 2018-01-01 hasta 2023-08-20
Crypto: `Singularitynet` | Datos Observados en el período desde 2018-01-21 hasta 2023-08-20
Crypto: `Fetch-AI` | Datos Observados en el período desde 2019-02-28 hasta 2023-08-20
Crypto: `Solana` | Datos Observados en el período desde 2020-04-10 hasta 2023-08-20
Crypto: `Render-Token` | Datos Observados en el período desde 2020-06-14 hasta 2023-08-20

#### Criterios de la Propuesta
1. Criptomonedas más rentables por Capitalización de Mercado.
2. Criptomonedas más rentables por YTD.
3. Criptomonedas por estabilidad **Stablecoins**

#### KPIs utilizados.

Para conseguir los objetivos planteados se recurrio al uso de indicadores de Gestión o KPI los cuales se presentan a continuación:
1. **Revalorización en lo que va de año YTD% (Year to date)** La revalorización en lo que va de año (YTD%) es un indicador que muestra el **rendimiento de una criptomoneda** desde el comienzo del año hasta la fecha actual. Es útil para evaluar el crecimiento o la pérdida de valor de una criptomoneda en un período específico y compararlo con otros activos o índices de referencia arrojando los siguientes resultados:
   ![ytd para el 2023](/img/ytd_2023.png)

   El gráfico arroja que las criptomonedas con mayor indice de rentabilidad son `Singularitynet`, `Fetch-AI` y `Render-Token` todas relacionadas con el boom de la **Inteligencia Artificial**, aunque no significa que se vayan a mantenerse en el tiempo, quizás se pueda aprovechar para obtener beneficios..
2. **Capitalización de Mercado** La capitalización de mercado es un indicador que muestra el valor total de todas las monedas en circulación de una criptomoneda. Es una medida importante para evaluar el tamaño y la popularidad de una criptomoneda en comparación con otras.
    ![cdm para el 2023](/img/cdm_2023.png)
3. **Dominancia de Mercado** La dominancia de mercado muestra la proporción de la capitalización de mercado de una criptomoneda específica en relación con la capitalización de mercado total de todas las criptomonedas.
   ![rdm para el 2023](/img/rdm_2023.png)

   Los dos indicadores anteriormente señalados muestran la preponderancia del `Bitcoin`en el ecosistema de las criptomonedas, teniendo la capitalización de mercado más alta superando los 500 mil millones de dolares y aportando con el 49% a la capitalización global del mercado.

4. **La volatilidad implícita** es una medida de las expectativas del mercado sobre la volatilidad futura de un activo subyacente, como una acción, un índice o una divisa. Esta medida se calcula a partir del precio de mercado de las opciones sobre el activo subyacente, utilizando un modelo matemático para estimar la volatilidad que se deriva del precio de estas opciones. La volatilidad puede darnos una visión general en los siguientes aspecto:
    * **Identificar oportunidades de trading**: La volatilidad implícita puede ayudar a identificar oportunidades de trading en criptomonedas. Si la volatilidad implícita es alta, puede indicar que se esperan grandes fluctuaciones en el precio de la criptomoneda en el futuro, lo que puede ser una oportunidad para comprar o vender en el momento adecuado.
    * **Evaluar el riesgo**: La volatilidad implícita también puede ser utilizada para evaluar el riesgo de una inversión en criptomonedas. Si la volatilidad implícita es alta, puede indicar que el activo tiene un mayor riesgo y una mayor incertidumbre en su comportamiento futuro, lo que puede ser un factor a considerar al tomar decisiones de inversión.
    * **Valorar opciones financieras**: La volatilidad implícita es un factor clave en la valoración de opciones financieras en criptomonedas. Los inversores pueden utilizar la volatilidad implícita para estimar el precio de las opciones y determinar si son una inversión atractiva.
Identificar tendencias: La volatilidad implícita también puede ser utilizada para identificar tendencias en el mercado de criptomonedas. Si la volatilidad implícita es alta, puede indicar que el mercado está experimentando una mayor incertidumbre y que los inversores están tomando posiciones más defensivas.

## Conclusiones:
Luego del análisis detallado realizado y en concordancia con las premisas y objetivos planteados se puede presentar las siguientes alternativas de inversión:
1. El grupo de **criptomonedas más rentables por capitalización de mercado** en vista de los resultados arrojados son las siguientes:
    * `Bitcoin` Es actualmente criptomoneda mejor valorada en el mercado nuestro análisis arroja su rubustes y fortaleza.
    * `Ethereum` Es una criptomoneda que ocupa el segundo lugar y además tiene otras utilidades, más allá de acumular valor con el tiempo, miles de proyectos de todo tipo, usan el token nativo de la red de Ethereum (ETH) lo que le da un poder sobre otros proyectos.
  
2. El grupo de **Revalorización en lo que va de año YTD% (Year to date)** en este grupo se señalan proyectos realcionados con Inteligencia Artificial que se han valorizado de manera importante en el período actual.
    * `Singularitynet` Es una plataforma de AI descentralizada y basada en la blockchain de Ethereum que permite a los desarrolladores y empresas crear, compartir y monetizar modelos de IA de manera segura y eficiente.
    * `Fetch-AI` Esta plataforma permite a los participantes crear y utilizar agentes autónomos (ordenadores con IA) para realizar tareas y transacciones en su nombre, resumiendo, realizar tareas y transacciones de manera más eficiente y automatizada.
3. El grupo de **Stablecoins** En este grupo se encuentra aquellas criptomonedas que son pensadas para mantener una estabilidad sin ningún tipo de salto no están pensadas para ganar dinero pero tienen otros muchos usos de los que se puede sacar provecho, como por ejemplo para intercambio con otras monedas, esperando a que el mercado híper volátil de las criptos se estabilice un poco.
    * `Tether` Tether (USDT) es una stablecoin diferente al resto, puesto que su fin es imitar el precio del dólar en el momento actual. Es decir, tener 100 USDT será igual que tener 100 dólares. Se trata de una criptomoneda más pensada para el uso y no para la inversión.
      ![vol_tether para el 2023](/img/vth_2023.png).

## Descargo de responsabilidades
La inversión en criptomonedas conlleva un **alto nivel de riesgo** y puede no ser adecuada para todos los inversores. Antes de tomar cualquier decisión de inversión, se recomienda encarecidamente que consulte a sus asesores financieros, de inversiones y fiscales profesionales para determinar si la inversión en criptomonedas es adecuada para usted.

Tenga en cuenta que la información proporcionada en este análisis es solo para fines informativos y no debe considerarse asesoramiento financiero o de inversión. No se garantiza que la información sea precisa, completa o actualizada en todo momento. No soy responsable de ninguna pérdida o daño que resulte de su confianza en la información proporcionada.

Tenga en cuenta que la inversión en criptomonedas puede conducir a la pérdida de capital durante períodos cortos o incluso largos. Solo debe invertir lo que pueda permitirse perder y debe comprender completamente los riesgos asociados con la inversión en criptomonedas antes de tomar cualquier decisión de inversión.
   

## Recomendaciones:

Este repositorio es de acceso **público** se recomienda:
1. Realizar `git clone https://github.com/villarrealfx/PI-Data-Analytics/tree/main`.
2. Crear un entorno virtual de trabajo con alguna herramienta python tal como [venv](https://docs.python.org/3/library/venv.html).
3. instalar las dependencias que se encuentran en el archivo `requirements.txt` utilizando el comando `pip install -r requirements.txt`.

Gracias por su interés en este proyecto, para cualquier comentario o sugerencia puede comunicarse por el correo eléctronico `villarreal.fx@gmail.com`

## Bibliografía
### Libros
1. Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow Concepts, Tools, and Techniques to Build Intelligent Systems (2019) Aurélien Géron Published by O’Reilly Media, Inc 
2. Pandas-Cookbook-eBook (2017) Theodore Petrou Packt Publishing
3. Data Engineering with Python (2020) Paul Crickard Packt Publishing

### Páginas web
1. [pandas-Python Data Analysis Library](https://pandas.pydata.org/)
2. [scikit-learn: machine learning in Python](https://scikit-learn.org/stable/)
3. [developers.google](https://developers.google.com/machine-learning/recommendation/content-based/basics?hl=es-419)
4. [Markdown Guide](https://www.markdownguide.org/basic-syntax/)
