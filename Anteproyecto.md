## Definición del problema

Dada la gran variedad existente de tecnologías de producción fotovoltaica, es comúnmente aceptada la necesidad de poder comparar el rendimiento de estos distintos sistemas de producción de energía eléctrica. Del mismo modo se hace necesario monitorizar la producción con el fin de detectar posibles deficiencias que impidan maximizar la producción energética.

Para poder comparar el rendimiento se necesita definier un procedimiento estándar de comparación de rendimiento, que debe estar disponible en la mayor cantidad porsible de situaciones.

Este método de comparación debería estar respaldado por una comparación detallada de las curvas I-V de los distintos generadores fotovoltaicos.

## Herramienta a utilizar

Para definir este estándar sería extremadamente útil el disponer de un sistema de medida basado en sistemas abiertos, lo que garantiza la reproductibilidad y la claridad en el proceso de medida. Es por ello que parece necesario utilizar dispositivos basados en open hardware (OH), cuyos diseños son totalmente publicos y abiertos, así como el software que utilizan, permitiendo que cualquiera pueda reproducir los experimentos y medidas.

El movimiento [OpenSource](http://opensource.org/), ha producido a día de hoy una amplia variedad de dispositivos, que van desde pequeños montajes basados en microcontroladores, del que [Arduino](http://arduino.cc) puede ser el máximo exponente, hasta desarrollos de servidores ([Open compute project de Facebook](http://www.opencompute.org/)). Importantes organizaciones científicas (como el CERN) y empresas (como Intel, ATMel o Texas Instruments), se han sumado a esta inciativa, como se puede ver en el [Open Hardware Repository](http://www.ohwr.org/) 

Uno de los desarrollo OH más existosos hasta el momento ha sido Arduino, una placa de prototipado rápido creado en torno a los microcontroladores de la serie ATMega (inicialmente ATMega168, ATMega328, ATMega1280 y ATMega2560) desarrollado por un grupo de ingenieros de diferentes paises, lo que evidencia también como la cultura abierta facilita la cooperación hasta el punto de desarrolar sistemas de forma totalmente abierta. En la [web del proyecto](http://www.arduino.cc/en/Main/Products) se puede encontrar toda la documentación necesaria para poder fabricar la mayoría de estos dispositivos electrónicos, incluyendo tanto los diseños de las placas de circuito impreso (PCB), así como todo el software necesario para utilizarlo y programarlo (tanto entorno de desarrollo como el bootloader y las librerías que se usan).

## Proyecto

El proyecto que se pretente realizar trata de desarrollar un sistema de medida basado en soluciones Open-Hardeare capaz de medir de forma sencilla las curvas I/V de sistemas fotovoltaicos en diferentes situaciones.

Existen distintas formas de medir el comportamiento de los sistemas, dependiendo principalmente de la historia de producción de las mismas, estando todas ellas expuestas a la irradiación solar:

Las placas están en plena producción, se desconectan de la planta en la que están incluídas y se conectan al aparato de medida. Es de suponer que al estar extrayendo energía de las placas utilizando el punto de máxima potencia (MTP) la temperatura de las placas será menor.
Las placas están en circuito abierto, y se conectan al sistema de medida para determinar sus curvas características. En este caso la placa no ha podido liberar toda la energía recibida, con lo que su temperatura será mayor.
Las placas están conectadas en cortocircuito. En ese caso se ha podido liberar parte de la energía, hay que determinar si su temperatura será ...

Es de suponer que la medida en un momento dado puede variar dependiendo del estado previo de producción de las placas. Para determinar la influencia de método de medida en el resultado final se pretende diseñar un protocolo experimental que cuantifica esta influencia:

Varios conjuntos de distintos tipos de placas se someterán a ciclos de producción y posteriormente se medirán sus curvas características IV con el dispositivo de medida basado en Arduino