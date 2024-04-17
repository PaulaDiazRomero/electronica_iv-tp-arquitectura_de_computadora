# Informe de Investigación Sobre Arquitectura de Computadoras

Electronica IV - TP - Arquitectura de Computadora

Paula Diaz Romero

## Introducción

Una computadora es un dispositivo electrónico que recibe todo tipo de datos y es capaz de procesarlos a gran velocidad.
En ella siempre se encuentran dos tipos de elementos indispensables para su funcionamiento: físicos y lógicos. Al conjunto de componentes físicos y elementos internos y externos de una computadora se lo denomina como hardware. Este es el que permite ejecutar el software, es decir, realiza la conversión de las instrucciones enviadas a la computadora a un lenguaje que ésta sea capaz de interpretar y así se puedan realizar las diferentes tareas.

La arquitectura de una computadora convencional está formada por los elementos que conforman el hardware y software, en otras palabras, la arquitectura de computadora es la organización lógica del hardware. En términos generales, sus componentes son:
- La unidad central de procesamiento (CPU)
- La unidad de memoria en la que residen datos y programas (UM)
- La unidad de buses (UB)
- Las unidades de entrada/salida o periféricos
- El programa de almacenado (instrucciones de la UM)

La arquitectura u organización de computadora también engloba la microarquitectura, es decir, no sólo abarca la estructura y el conjunto de instrucciones constituyentes a la computadora sino también el conjunto de principios que describen las características de los componentes del hardware y cómo estos se interconectan e interactúan entre sí, ya que el funcionamiento de la computadora implica una fuerte cooperación entre las unidades que la componen.


## Clases de arquitectura de computadora

Entre los diversos modelos de arquitectura podemos encontrar la máquina de pila, un modelo sencillo de instrucciones cortas que se basa en apilar datos en la memoria; la máquina de registros, la cual se basa en usar múltiples registros con una única dirección donde el acceso a los datos será rápido y veloz; y, la máquina de acumulador, en la cual el acumulador es un registro en el cual se almacenan temporalmente los datos de resultados aritméticos y lógicos que despues procesará la ALU y, a diferencia del modelo anterior, este será más lento. Otras de las arquitecturas más populares son:

- **Arquitectura Von Newmann:** Es una de las arquitecturas fundamentales en el campo. Se basa en la idea de tener una unidad central de procesamiento que accede a una única memoria donde se almacenan tanto los datos como los programas. Las instrucciones y datos se guardan en la misma memoria y se recuperan a través de un bus común. Esta idea de unicidad imposibilita leer una instrucción mientras se ejecuta otra, por otro lado, todas las instrucciones pasan por la ALU causando una congestión y retraso de las siguientes etapas. Aún con todo esto, es la arquitectura más extendida hoy en día debido al amplio conjunto de programas desarrollados para ella.

- **Arquitectura Harvard:** A diferencia de la arquitectura de Von Newmann, esta arquitectura tiene la principal característica de utilizar memorias y buses separados para instrucciones y datos, lo que permite a la CPU un acceso simultáneo a ambos, mejorando el rendimiento de ciertas aplicaciones y, por lo tanto, teniendo una mayor velocidad de procesamiento.

- **Arquitectura RISC (Reducesd Instruction Set Computer):** Es un enfoque de diseño de procesadores que se caracteriza por utilizar un conjunto de instrucciones reducido y optimizado, además, sólo las instrucciones de carga y almacenamiento acceden a la memoria de datos. El diseño de máquinas con esta arquitectura posibilita el paralelismo en la ejecución de instrucciones y reduce los accesos a la memoria, con lo cual puede alcanzar altos niveles de rendimiento y eficacia.

- **Arquitectura CISC (Complex Instruction Set Computer):** A diferencia de RISC, los procesadores CISC utilizan un conjunto de instrucciones más amplio y diverso, permitiendo ejecutar operaciones más complejas. Sin embargo, este tipo de arquitectura dificulta el paralelismo de instrucciones, por lo que, en la actualidad, la mayoría de los sistemas CISC de alto rendimiento implementan un sistema que convierte las instrucciones complejas en varias instrucciones simples del tipo RISC, llamadas microinstrucciones.

- **Arquitectura EPIC (Ecplicitly Parallel Instruction Computing):** A diferencia de RISC y CISC, esta arquitectura permite agrupar instrucciones para ejecutarlas de manera paralela en forma explícita, es decir, se organiza la ejecución de instrucciones de bifurcación, donde el compilador planifique los caminos posibles de la ramificación y ambas ramas se ejecuten en el procesador en forma simultánea. Este diseño tiene como objetivo mejorar el rendimiento y eficiencia del sistema informático al dividir tareas en partes mas pequeñas y asignarlas a diferentes ramas para que se procesen en conjunto.

- **Arquitectura ARM:** Es una arquitectura RISC de 32 y 64 bits, desarrollada por ARM Holdings. Esta se usa para fabricar microprocesadores tanto simples y de bajo consumo como los que requieren más potencia. Dado su conjunto de instrucciones simples, estos procesadores no requieren de un gran procesamiento de datos, por lo que consumen pocos recursos y energía, pero, por otro lado, su rendimiento no es tan alto como en otras arquitecturas. Una de las últimas versiones, la ARMv7, admite implementaciones que adaptan la arquitectura a los requerimientos del mercado. Para aprovechar al máximo esto, se introdujo la ARMv7-M, diseñada para implementación de microcontroladores, complementando sus fortalezas en alto rendimiento.

- **Arquitectura Intel x86:** Es la arquitectura de procesadores responsable de la mayoría de los sistemas de computación del mundo. Se basan en una arquitectura CISC, manejando un conjunto amplio de instrucciones, por lo que, a diferencia de los procesadores ARM, los procesadores Intel requerirán más energía, pero tendrán un rendimiento superior en términos de potencia de procesamiento.

La diversas arquitecturas de computadoras ofrecen una variedad de beneficios que impulsan el desarrollo tecnológico y mejoran la experiencia del usuario.


## Partes de una arquitectura de computadora

Para entender mejor la estructura de la computadora, desarrollaremos los conceptos de cada uno de sus componentes:

- **La Unidad Central de Procesamiento (CPU)**: Es el procesador que controla las operaciones básicas de la computadora, enviando y recibiendo señales de control, direcciones de memoria y datos de un lugar a otro a través del bus. Sus componenetes fundamentales son:
  - La Unidad de Control (UC): Es la que interpreta las instrucciones y genera las señales de control para que se ejecuten.
  - La Unidad Aritmético Lógica (ALU): Es la que realiza las operaciones aritmético-lógicas y almacena los resultados en la memoria.
  - Los Registros: Son usados para almacenar temporalmente la información necesaria para el procesamiento (datos, direcciones, instrucciones).

- **La Unidad de Memoria**: Es la que almacena programas y datos. Es, principalmente, una memoria RAM de lectura/escritura.

- **La Unidad de Buses**: El bus es el canal de comunicación entre todas las unidades del sistema. Se compone de varias líenas por las que circula la información. Según la información que circula por el mismo, el bus se divide en:
  - Bus de datos: Transporta operandos o instrucciones entre los componentes de la computadora.
  - Bus de direcciones: Transmite las direcciones de las posiciones de memoria y de los dispositivos conectados.
  - Bus de control: Trnasporta señales de control que indican qué tipo de información viaja por el bus.

- **Unidad de Entrada/Salida**: Son vías que se encargan de interconectar los dispositivos externos (periféricos) con la computadora, por los cuales podremos ingresar o extraer información a o desde la CPU.

- **El Programa de Almacenado**: Es un conjunto de instrucciones almacenadas en la Unidad de Memoria. Las instrucciones son propias de cada máquina y se conocen como Set de Instrucciones.


## Conclusiones

En base a todo lo desarrollado, podemos concluir que la arquitectura de computadoras se trata de un conjunto de principios y estándares que definen la estructura y el diseño de los componentes de hardware y software que conforman un sistema informático, abarcando todos los niveles de sistemas, desde los circuitos electrónicos hasta los sistemas operativos y las aplicaciones. Su función es la de crear un sistema óptimo y eficiente y su implementación es esencial para definir la velocidad y consumo de energía de una computadora. 
Si descomponemos un sistema de cómputos en capas, la arquitectura de computadoras estaría entre los primeros niveles ya que es la base de la estructura y diseño del sistema y sus interconexiones, aunque estará presente en todos los niveles de capas.
A la hora de elegir una arquitectura de computadora, se debería considerar, al menos, las operaciones que realizaría la máquina, la compatibilidad entre los sistemas y componentes que se usarían, la densidad de datos con la que se operaría y la velocidad que se requeriría para su procesamiento.


## Bibliografía

- Ing. Ledda Larcher (2007). *¿Qué es una computadora?* Apuntes del Laboratorio de Informática Facultad de Agronomía y Agroindustrias. Universidad de Santiago del Estero.
http://faa.unse.edu.ar/apuntes/ccaunidad1.pdf

- Departamento de Cs. e Ing. de la Computación. *Introducción a la Operación de Computadoras Personales*. Universidad Nacional del Sur.
https://cs.uns.edu.ar/materias/iocp/downloads/Apuntes/Unidad%201%20-%20Hardware.pdf

- Daniel M. Argüello, Santiago C. Pérez e Higinio A. Facchini (2022). *Arquitectura de computadoras*. Universidad Tecnológica Nacional – Facultad Regional Mendoza.
https://www.researchgate.net/publication/349928725_ARQUITECTURA_DE_COMPUTADORAS_-_10_Edicion_-_2022

- Guillermo Bosque Perez, Nekane Azkona Estefanía (2018). *Estructura y Arquitectura
de Computadores*. Universidad del País Vasco.
https://web-argitalpena.adm.ehu.es/pdf/UWLGIN7192.pdf

- Patricia Quiroga (2010). *Arquitectura de computadoras*. 1era edición. Buenos Aires, Argentina.

- William Stallings (2005). *Organización y arquitectura de computadores*. 7ma edición. Madrid, España.

- ARM (2006-2008, 2010, 2014, 2017, 2021). *Armv7-M Architecture Reference Manual.*

- Sergio Hernán Rocabado Moreno, Daniel Arias Figueroa (2009). *Arquitectura y organización de la computadora.* 1era edición. Salta, Argentina.
https://libros.unlp.edu.ar/index.php/unlp/catalog/view/168/144/488-1

