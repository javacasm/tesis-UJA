## Definición del problema

Dada la gran variedad existente de tecnologías de producción fotovoltaica, es comúnmente aceptada la necesidad de poder comparar el rendimiento de estos distintos sistemas de producción de energía eléctrica. Del mismo modo se hace necesario monitorizar la producción con el fin de detectar posibles deficiencias que impidan maximizar la producción energética.

Para poder comparar el rendimiento se necesita definier un procedimiento estándar de comparación de rendimiento, que debe estar disponible en la mayor cantidad porsible de situaciones.

Este método de comparación debería estar respaldado por una comparación detallada de las curvas I-V de los distintos generadores fotovoltaicos.

## Herramientas a utilizar

Para definir este estándar sería extremadamente útil el disponer de un sistema de medida basado en sistemas abiertos, lo que garantiza la reproductibilidad y la claridad en el proceso de medida. Es por ello que parece necesario utilizar dispositivos basados en Open Hardware, cuyos diseños son totalmente publicos y abiertos, así como el software que utilizan, permitiendo que cualquiera pueda reproducir los experimentos y medidas.

El movimiento [OpenSource](http://opensource.org/), ha producido a día de hoy una amplia variedad de dispositivos, que van desde pequeños montajes basados en microcontroladores, del que [Arduino](http://arduino.cc) puede ser el máximo exponente, hasta desarrollos de servidores ([Open compute project de Facebook](http://www.opencompute.org/)). Importantes organizaciones científicas (como el CERN) y empresas (como Intel, ATMel o Texas Instruments), se han sumado a esta inciativa, como se puede ver en el [Open Hardware Repository](http://www.ohwr.org/) 

Uno de los desarrollos OH más existosos hasta el momento ha sido Arduino, una placa de prototipado rápido, barata y sencilla de programar y usar, que utiliza microcontroladores de la serie ATMega (inicialmente ATMega168, ATMega328, ATMega1280 y ATMega2560), desarrollado por un grupo de ingenieros de diferentes paises, lo que evidencia también como la cultura abierta facilita la cooperación, y que ha permitido crear proyectos moderamente avanzados a un público que hasta hace poco se sentía incapaz de ello. En la [web del proyecto](http://www.arduino.cc/en/Main/Products) se puede encontrar toda la documentación necesaria para poder fabricar la mayoría de estos dispositivos electrónicos, incluyendo tanto los diseños de las placas de circuito impreso (PCB), así como todo el software necesario para utilizarlo y programarlo (tanto entorno de desarrollo como el bootloader y las librerías que se usan).

Otro de estos proyectos que más conseguido acercar al público al mundo de la programación y de los proyectos electrónicos ha sido [Raspberry Pi](https://www.raspberrypi.org/), una placa de pequeño tamaño, que contiene un ordenar de la capacidad de un portatil y que se puede adquirir al competivo precio de 25$ y desarrollado con la idea de acercar la programación a todo el público y sobre todo de incluirla en la educación de los más pequeños. Su bajo coste no ha impedido que se use para crear [cluster de computación](http://makezine.com/2013/06/05/33-rpi-beowulf-cluster/) hasta hace poco impensables, sino que ha facilitado su uso como [registrador de datos](https://github.com/abelectronicsuk/ABElectronics_Python_Libraries/tree/master/ADCPi)

Animados por el éxito de la filosofía open ha aparecido nuevos proyectos y desarrollos, cada vez más avanzados y con mayor capacidad de procesamiento y bajo coste.

## Proyecto

Revisando la bibliografía existente, se ve que no existe una única formas de medir el comportamiento de los sistemas fotovoltaicos. Citemos las que parecen más utilizadas:

* Las placas están en plena producción, se desconectan de la planta en la que están incluídas conectando al aparato de medida. Es de suponer que al estar extrayendo energía de las placas utilizando el punto de máxima potencia (MTP) la temperatura de las placas será menor.

* Las placas están en circuito abierto, y se conectan al sistema de medida para determinar sus curvas características. En este caso la placa no ha podido liberar toda la energía recibida, con lo que su temperatura será mayor.

* Las placas están conectadas en cortocircuito. En ese caso se ha podido liberar parte de la energía.

A primera vista parece lógico pensar que los resultados serán muy diversas, dado que influirán tando las condiciones actuales (sólo hay que ver sus distintas temperaturas) así como lo que podemos  denominar "sus historias productivas", es decir el tiempo y la forma en que han estado expuestas a la irradiación solar.

Es por esto que el proyecto que se va a realizar va a desarrollar un sistema de medida basado en soluciones Open-Hardeare capaz de comparar de forma sencilla las curvas I/V de sistemas fotovoltaicos en estas situaciones diferentes de manera sencilla.

Para determinar la influencia de método de medida en el resultado final se pretende diseñar un protocolo experimental que cuantifique esta influencia:

Varios conjuntos de distintos tipos de placas se someterán a ciclos de producción y posteriormente se medirán sus curvas características IV con el dispositivo de medida basado en Open-Hardware 

## Objetivos

* Desarrollar una plataforma Open Hardwar de medida, utilizando sistemas abiertos y de bajo coste

* Definir un protocolo de medida para distintos sistemas de placas

* Realizar una campaña de medida con sistemas fotovoltaicos en distintas situaciones, utilizando el protocolo de medida y el sistema desarrollado

* Comparar lo resultados de los distintos sistemas de medida.