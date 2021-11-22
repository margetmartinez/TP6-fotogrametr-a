# Laboratorio 6

## Introducción

1. Transmitancia

Corresponde a la luz incidente que pasa a través de una superficie receptora. Esta corresponde a un valor que mide la cantidad de luz o ondas que pasan de un lado a otro de una superficie. Para así, comparar la cantidad de luz que entra con la cantidad de luz que sale del objeto.

2. Radiancia

Esta describe la cantidad de radiación o de energía que es enviada o emitida por un área o superficie emisora en particular, en una dirección con un ángulo sólido hacia el sensor en una dirección específica. Los cuerpos emiten radiación en todo el intervalo del espectro solar, más que todo en la zona del infrarrojo. Por lo que si se mide la radianza de un cuerpo con todo el espectro electromagnético, lo que se obtiene es la radianza espectral del cuerpo. El máximo nos indicaría la temperatura del cuerpo. Esta se mide en unidades radiométricas W/m2 sr, por ser un ángulo sólido (Lira & Guevara, 2017).

3.  Cuerpos negros

De acuerdo a la lectura vista en clase, estos son radiadores hipotéticos e ideales que absorben y remiten totalmente toda la energía que incide sobre él. En este caso, si el cuerpo emisor de la radiación cumple con las características de cuerpo negro que está en equilibrio termodinámico, esta radiación se llama “radiación de cuerpo negro”. Esta energía radiante va a depender de la temperatura y la longitud de onda. Por otro lado, la **emisividad** es un coeficiente que se encarga de medir la eficiencia con la que un objeto llega a irradiar energía y a su vez la compara con la eficicencia de un cuerpo negro. Los materiales reales no se comportan como un cuerpo negro, debido a que ningún material es capaz de aborver toda la energía que llega a él y tampoco irradia toda la energía que recibe, sólo una fracción de esta. Como vemos, los objetos emiten la energía de manera distinta, por ejemplo, un cuerpo a temperatura ambiente no emite mucha energía radiante y sus longitudes de onda suelen ser más largas que el espectro visible. Conforme aumenta la temperatura, la energía emitida es mayor. También, las superficies más oscuras y de textura “mate” tienden a emitir más energía que las superficies brillantes. Por lo que de acuerdo a la ley de Kirchhoff, estos cuerpos que son buenos emisores de energía, son también buenos absorbentes. 

4. Aplicaciones que tiene la teledetección térmica

- Teledetección térmica para la obtención de la temperatura del suelo con gvSIG

En el taller titulado *“Teledetección térmica de imágenes Landsat históricas con gvSIG”* realizado por la Escuela de Geografía de la Universidad de Costa Rica, utilizaron la teledetección térmica para obtener la temperatura del suelo a partir de los valores de brillo de la banda térmica de las imágenes satelitales. Para ello, primero se corrigieron los efectos de la absorción atmosférica y de la emisividad de la superficie. Por ello se obtiene un mapa de emisividad a partir de un índice de vegetación al cual se le realizan cálculos con la calculadora raster para obtener el mapeado de la emisividad de la imagen. Luego se transforman los niveles digitales de la imagen a radiancia relacionada con el terreno, este paso es fundamental para poder comprar datos de múltiples sensores. Por lo que luego se obtiene la temperatura superficial a partir de radiancias. 

![image](https://github.com/margetmartinez/TP6-fotogrametr-a/blob/main/gvSIG.png)

La primera imágen de izquierda a derecha, muestra como la máxima emisividad corresponde a las áreas de gran cantidad de vegetación, mientras que la mínima es por el agua. La segunda muestra un ráster con radiancias corregidas, que reduce los efectos atmosféricos y muestra valores referidos al terreno. La última representa un mapa donde los valores de píxel representan las temperaturas del suelo en grados Celsius.

- Teledetección térmica para el estudio de la dinámica de inundación con AHS

En el artículo titulado *”Teledetección térmica en la Reserva Biológica de Doñana”* se utilizaron imágenes de alta resolución mediante el sensor AHS junto con la colocación de radiómetros térmicos para obtener datos diarios y así calibrar y validar periódicamente las imágenes proporcionadas por los satélites. Por lo que se procedió a caracterizar radiometricamente las distintas superficies presentes en la Reserva Biológica de Doñana a través de la medida de espectros de reflectividad y emisividad. También se realizaron productos de temperatura y emisividad de la superficie terrestre derivados también por las imágenes AHS y obtenidos mediante el algoritmo Temperature and Emissivity Separation (TES).

![image](https://github.com/margetmartinez/TP6-fotogrametr-a/blob/main/AHS.png)

La imagen muestra la temperatura de la superficie terrestre y un constraste espectral para una región cercana a la costa realizado en una imagen AHS en 2008.

- Teledetección térmica para detección de incendios forestales con NOAA/16-AVHRR

En el artículo *”Detección de incendios forestales utilizando imágenes NOAA/16-LAC en la Región de La Araucanía, Chile”*, se utilizaron imágenes satelitales para la detección de fuegos forestales. Para ello se analizaron 33 imágenes pertenecientes al sensor NOAA/16-AVHRR, siendo uno de los más utilizados para la detección de incendios forestales debido a sus tres bandas térmicas. Esto es posible gracias a que las fuentes de alta temperatura provocan un notable incremento en la radiación emitida en las longitudes de onda, lo que permite que se perciban hasta una porción de píxel. A pesar de ello se presentan complicaciones debido a que detectan más que todo el fuego y no las áreas ya quemadas, esto debido a la disminución de la temperatura en estas áreas, lo que reduce la reflectancia.

![image](https://github.com/margetmartinez/TP6-fotogrametr-a/blob/main/NOAA.png)

La imagen muestra los resultados de la detección de incendios. En la imagen A) se pueden ver como rombos blancos y en la B) como rombos negros. Se puede observar una detección fallida debido a que capta las nubes erróneamente como un punto de fuego.

## Serie Temporal 2000-2016
### Gráficos
![imagen](Graficos2000.png)
### Mapa
![imagen](Mapa2000.png)
### Resultados y Análisis
1. Como se puede observar en gráficos y mapas, a través de Google Earth Engine se pueden manejar, representar y analizar grandes volúmenes de datos. Para este primer caso, se está representando una serie temporal de 16 años, lo que permite observar la variabilidad de los datos a lo largo de este periodo. 
2. En el primer gráfico (Temperatura de día), hay mucha variabilidad de datos. Estos van desde picos altos 32°C y un solo pico bajo de 21°C aproximadamente. La temperatura promedio es de 28°C. En el segundo gráfico (Temperatura de noche), la temperatura es más constante. Se mantiene entre 20°C. Se registran picos altos de 26°C y picos bajos de 10°C aproximadamente. 
2. En ambos mapas podemos ver cómo se distribuyó la temperatura de la superficie en este periodo. Se identifican dos patrones claros. Las altas temperaturas durante el día se registraron en la zona de Guanacaste principalmente. Mientras que las temperaturas más bajas se registraron en la cordillera de Talamanca. Durante la noche se repite este mismo patrón.  


## Serie Temporal Enero-Diciembre 2015
### Gráficos
![imagen](Graficos2015.png)
### Mapa
![imagen](Mapa2015.png)
### Resultados y Análisis
1. En esta serie temporal, al ser mucho menos datos que la serie anterior. Se puede ver con más detalle el comportamiento de la temperatura a lo largo de 12 meses. Por ejemplo, es más fácil identificar la época seca de la época lluviosa. 
2. En el primer gráfico (Temperatura de día), hay una mayor variabilidad. Los picos de temperatura se registran durante los meses de marzo, abril y mayo, llegando a 32°C aproximadamente. A partir de junio la temperatura desciende y en agosto hasta octubre es constante. Hasta que se llega a noviembre y se registra el pico más bajo de 26°C aproximadamente. 
3. El segundo gráfico (Temperatura de noche), prácticamente es constante durante todo el año, con excepción de tres picos bajos. El primero de 13°C (el más bajo de todos) registrado en junio, el segundo de 14°C registrado entre julio y agosto y el último de 17°C registrado entre octubre-noviembre. 
4.   En los mapas, se observa cómo las temperaturas altas se distribuyen en las zonas bajas, principalmente en la provincia Guanacaste. Y las temperaturas bajas se distribuyen en las zonas altas como las cordilleras, principalmente en la cordillera de Talamanca. 


## Caso de Estudio: Sequía Región Chorotega (2014-2015)
### Gráficos
![imagen](GraficosCaso.png)
### Mapa
![imagen](Mapa2014.png)
### Resultados y Análisis 
1. Los gráficos muestran que las máximas temperaturas en la región Chorotega se registraron durante el primer semestre del año 2015. La máxima temperatura fue de 35°C en el mes de abril. Pero desde el inicio del mes de marzo la temperatura tuvo un ascenso y se mantuvo constante hasta el mes de julio cuando descienden. En el mes de junio se registra la temperatura más baja de 25°C. El segundo periodo en el cual se registraron altas temperaturas, es de nuevo el primer semestre pero del año 2014. En este periodo las temperaturas altas son más constantes que las del año 2015, pero se mantuvieron por debajo de los 35°C. Sin embargo, las temperaturas no bajaron de los 27°C. 

2. Para los segundos semestres tanto del 2014 como del 2015, las temperaturas estuvieron entre los 24°C y 32°C. Siguiendo un patrón de descenso desde julio hasta diciembre. Con estos resultados, se refleja la estacionalidad climática. Los primeros seis meses del año son más calientes y se relaciona con la época seca; en el segundo semestre los meses son más fríos relacionado con la época lluviosa. Aunque, claramente también están relacionadas con otros fenómenos climáticos como el ENOS o el fenómeno de la Niña, entre otros. 

3. Los mapas apoyan los gráficos, y se observa la distribución de las temperaturas coincidiendo en los cuatro periodos. Pero principalmente, lo que se señaló anteriormente, los primeros semestres registraron las más altas temperaturas. Siendo el primer semestre del 2015 el de temperaturas más altas. Estas altas temperaturas se registraron en su mayoría en las zonas urbanas, planicies y cerca de las costas. 

4. Con lo mencionado anteriormente, los momentos de sequía severa se pueden dar durante el primer semestre del año. Se concentra específicamente de marzo a mayo. Si el Instituto de Acueductos y Alcantarillados desea prepararse mejor para futuras sequías, debe tomar medidas para este periodo del año. 

## Conclusiones

Como vimos anteriormente, la teledectección térmica nos permite realizar distintos tipos de estudio en la superficie terrestre debido a sus características de radiancia. Podemos realizar desde monitoreos de incendios forestales hasta estudiar la dinámica de inundaciones de una región. Parte de esto se pudo observar en el estudio de caso de la región Chorotega con el monitoreo de sequías. Gracias a ello pudimos localizar las áreas donde se concentra mucho más la temperatura y que indican una pérdida de vegetación y aumento de incendios forestales.Al conocer los focos de temperatura, es posible un mejor manejo y una respuesta mucho más rápida ante eventuales eventos de sequía en próximos años. 

Por otro lado, con las series temporales podemos elevar los estudios y análisis a otro nivel, ya que con estos podemos estudiar patrones y comportamientos de distintos factores en la superficie terrestre en un periodo determinado de tiempo. Como lo vimos en los dos casos expuestos anteriormente, este nos permite observar esos picos de temperatura y por ende, estudiar y analizar la fuente o la causa de ello. Es por esto que combinar ambas da una resultado muy beneficioso para los diversos estudios de la Tierra.
