Dada la gran variedad existente de tecnologías de producción fotovoltaica, es comúnmente aceptada la necesidad de poder comparar el rendimiento de estos distintos sistemas de producción de energía eléctrica. 

Para poder comparar el rendimiento se necesita desarrollar un procedimiento que sea lo más estándar posible, para así poder disponer de él el cualquier entorno.

Para definir este estándar sería útil el poder tener un sistema de medida basado en sistemas lo más abiertos posible. Una forma  de garantizar la reproductibilidad y la claridad en el proceso de medida es utilizar dispositivos basados en open hardware (OH), cuyo esquemas están totalmente abierto y disponibles para que cualquiera pueda reproducir los experimentos y medidas.

El movimiento opensource, ha producido a día de hoy una amplia variedad de dispositivos, que van desde pequeños montajes basados en microcontroladores hasta desarrollo de servidores ¿Facebook hardware? 

Uno de los desarrollo OH más existosos hasta el momento ha sido Arduino, una placa de prototipada rápido creado en torno a los microcontroladores de la serie ATMega (inicialmente ATMega168, ATMega328, ATMega1280 y ATMega2560) desarrollado por un grupo de ingenieros de diferentes paises. En la web del proyecto se puede encontrar toda la documentación necesaria para poder crear los equipos electrónicos, incluyendo por supuesto los diseños de las placas de circuito impreso (PCB), así como todo el software necesario para programarlo (tanto entorno de desarrollo como el bootloader y las librerías que se usan)

El proyecto que se pretente realizar trata de desarrollar un sistema de medida basado en Arduino capaz de medir de forma sencilla las curvas I/V de diferentes sistemas fotovoltaicos.


Existen distintas formas de medir el comportamiento de los sistemas, dependiendo principalmente de la historia de producción de las mismas, estando todas ellas expuestas a la irradiación solar:

Las placas están en plena producción, se desconectan de la planta en la que están incluídas y se conectan al aparato de medida. Es de suponer que al estar extrayendo energía de las placas utilizando el punto de máxima potencia (MTP) la temperatura de las placas será menor.
Las placas están en circuito abierto, y se conectan al sistema de medida para determinar sus curvas características. En este caso la placa no ha podido liberar toda la energía recibida, con lo que su temperatura será mayor.
Las placas están conectadas en cortocircuito. En ese caso se ha podido liberar parte de la energía, hay que determinar si su temperatura será ...

Es de suponer que la medida en un momento dado puede variar dependiendo del estado previo de producción de las placas. Para determinar la influencia de método de medida en el resultado final se pretende diseñar un protocolo experimental que cuantifica esta influencia:

Varios conjuntos de distintos tipos de placas se someterán a ciclos de producción y posteriormente se medirán sus curvas características IV con el dispositivo de medida basado en Arduino