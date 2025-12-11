# Descubriendo perspectivas sobre la industria del taxi en Chicago: un análisis exhaustivo de datos del Proyecto Zuber

El "Proyecto Zuber" ofrece un análisis profundo de la dinámica de la industria del transporte compartido, centrándose en comprender las preferencias de los pasajeros y el efecto de factores externos, como las condiciones climáticas, en la duración de los viajes. Este análisis exhaustivo proporciona información valiosa para optimizar los servicios tanto para conductores como para pasajeros, a la vez que muestra las tendencias competitivas en el sector del taxi. Mediante una meticulosa preparación de datos, un análisis exploratorio de datos y la comprobación de hipótesis, descubrimos patrones que pueden influir en las decisiones estratégicas de las partes interesadas.

Preparación de datos
Antes de comenzar el análisis, comenzamos a preparar los datos para garantizar su calidad y usabilidad. Este paso implicó cargar varios marcos de datos con detalles sobre viajes completados, compañías de taxis y condiciones meteorológicas. Tras las comprobaciones iniciales, confirmamos que los conjuntos de datos no presentaban valores faltantes.

Revisamos los conjuntos de datos en busca de duplicados y descubrimos que, si bien df01 y df04 no tenían ninguno, df07 contenía duplicados justificados. Una vez completados estos pasos, los datos se prepararon para el análisis.

Contenido del artículo


Contenido del artículo
Los 10 mejores barrios según los recorridos realizados
El análisis de los puntos de llegada más populares en Chicago ofrece información significativa sobre el comportamiento y las preferencias de los pasajeros. Al examinar el número de viajes completados a diversos barrios, identificamos áreas clave que desempeñan un papel fundamental en la demanda de viajes compartidos.

Los datos revelaron que:


El Loop se convirtió en el punto de llegada más popular, con un promedio de viajes muy superior al de otros barrios. Este hallazgo subraya la importancia de la zona, probablemente debido a su carácter comercial y empresarial.
River North y Streeterville le siguieron como destinos populares, lo que indica una sólida demanda en áreas conocidas por su entretenimiento, gastronomía y actividades residenciales.
El Aeropuerto Internacional O'Hare , aunque combinado asociado con los viajes, se aseguró un lugar entre los cinco primeros, pero tuvo un promedio de viajes más bajo en comparación con las ubicaciones del centro de la ciudad.
Contenido del artículo
Estos datos son valiosos para las empresas de taxis y viajes compartidos que buscan optimizar sus servicios centrándose en zonas de alta demanda. Comprender estos patrones permite una mejor asignación de recursos y una mayor satisfacción del cliente.

Las 10 principales compañías de taxis por cantidad de viajes
El panorama competitivo entre las compañías de taxis en Chicago muestra el dominio de ciertas empresas en el mercado. Al analizar el número de viajes completados por diversas compañías, observamos lo siguiente:


Flash Cab lideró con el mayor número de viajes registrados, lo que indica su importante participación de mercado y alcance de clientes.
Taxi Affiliation Services y Medallion Leasing también mostraron un sólido desempeño, destacando su importante presencia en el mercado.
Empresas como Yellow Cab y Taxi Affiliation Service Yellow mostraron una competitividad considerable, manteniendo una participación notable en los viajes completados.
Contenido del artículo
Estos hallazgos ayudan a las partes interesadas a comprender qué empresas lideran el mercado e identificar tendencias que podrían influir en las estrategias competitivas.

Prueba de hipótesis: el impacto del clima en la duración de los viajes
Una parte crucial del Proyecto Zuber consistió en investigar el impacto de las condiciones meteorológicas en la duración de los viajes. En concreto, probamos las hipótesis de que los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare los sábados lluviosos tendrían una duración promedio diferente a la de los viajes los sábados sin lluvia.

Hipótesis:


Hipótesis Nula (H0) : Los sábados lluviosos no afectan la duración media de los viajes.
Hipótesis alternativa (H1) : Los sábados lluviosos sí afectan la duración promedio de los viajes.
Metodología:

Filtramos el conjunto de datos (`df07`) para incluir únicamente los datos de los sábados y lo dividimos en dos grupos: uno representa los sábados lluviosos y otro los sábados sin lluvia. Realizamos una prueba t para comparar la duración promedio de los viajes entre estos dos grupos, utilizando un nivel alfa de 0,05 para determinar la significancia.

Resultados:


La prueba T arrojó una estadística T de aproximadamente 7,19 y un valor P de 6,74e-12 , que está significativamente por debajo del umbral de 0,05.
Esto nos llevó a rechazar la hipótesis nula , concluyendo que el clima lluvioso tiene un impacto significativo en la duración de los viajes.
Contenido del artículo
Verificación de supuestos de variación: prueba de Levene
Para garantizar la solidez de nuestros hallazgos, realizamos la prueba de Levene para verificar la igualdad de variaciones entre los dos grupos.

Resultados de la prueba de Levene:


La prueba arrojó una estadística de prueba de Levene de 0,39 y un valor P de 0,533 , lo que indica que no hay diferencias significativas en las varianzas.
Esto confirmó que era apropiado utilizar una prueba T estándar, pero ya habíamos optado por la prueba T de Welch, más conservadora, para lograr mayor confiabilidad.


Contenido del artículo
Interpretación:

La ausencia de diferencias significativas en la varianza reafirmó la solidez de nuestros resultados. El valor p extremadamente bajo de la prueba T confirma que la duración de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare es mayor los sábados lluviosos. Esta información puede ser crucial para la planificación y gestión de servicios, especialmente durante condiciones climáticas adversas.

**CONCLUSIÓN**

Hay evidencia estadisticamente significativa de que la duración promedio 
de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare 
ES DIFERENTE los sábados lluviosos comparado con sábados no lluviosos.

*Basado en:*

• La diferencia de 413.93 segundos (6.90 minutos) es estadísticamente 
  significativa
  
• El clima (lluvia/tormenta) SÍ afecta la duración de los viajes

• Zuber debería considerar este factor en su modelo de negocio


*Recomendaciones:*
1. Ajustar tiempos estimados en días lluviosos
2. Aumentar precio sugerido en sábados lluviosos (mayor demanda/duración)
3. Comunicar a usuarios que viajes pueden tardar más en lluvia
