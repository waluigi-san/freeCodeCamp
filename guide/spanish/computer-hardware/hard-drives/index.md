---
title: Storage Drives
localeTitle: Unidades de almacenamiento
---
## Unidades de disco duro (HDD)

Los discos duros son dispositivos de almacenamiento permanente para computadoras. Hay varios tipos de unidades de disco duro: discos magnéticos tradicionales, discos de estado sólido de nueva generación o discos híbridos que contienen SSD y almacenamiento magnético.

Los discos duros tradicionales utilizan agujas magnéticas y platos giratorios magnetizados para almacenar datos. Debido a estas partes móviles, los discos duros se dañan fácilmente por caídas y / o golpes. El motor que gira los platos también consume mucha energía y, sin embargo, ningún otro método de almacenamiento es tan asequible para grandes volúmenes de almacenamiento.

Los discos duros vienen en varias capacidades de almacenamiento, y algunos incluso almacenan 10 TB (10 billones de bytes). Las computadoras típicas vienen con 256 GB (256 millones de bytes) a 1 TB de espacio de almacenamiento. Las computadoras portátiles generalmente usan unidades de estado sólido (SSD) porque son más rápidas, más ligeras y no tienen partes móviles, lo que las hace menos propensas a fallar debido al impacto. Para la misma cantidad de almacenamiento, los SSD son generalmente más caros que los discos duros. Recientemente, se han lanzado algunos SSD que interactúan con la placa base a través de la ranura del bus PCIe (PCI Express) utilizando un sistema llamado NVMe. Estos SSD han demostrado ser incluso más rápidos en los tiempos de lectura / escritura que los SSD SATA tradicionales.

Los cabezales magnéticos son responsables de leer y escribir datos, que se almacenan físicamente en un conjunto de discos revestidos magnéticamente apilados uno encima del otro, lo que se conoce como un disco. Las cabezas se encuentran al final de una armadura. Los discos interiores de la fuente tienen dos cabezas en un solo brazo. Esto permite acceder a los datos desde ambos discos, por debajo y por encima del brazo. Los discos superior e inferior de la fuente solo tienen una cabeza al final de un brazo. En el extremo opuesto del brazo hay un actuador. Proporciona el movimiento del brazo para desplazarse desde el centro de la bandeja, el eje, hasta las regiones más externas de la bandeja. La cantidad de tiempo que se tarda en colocar la cabeza en la ubicación concéntrica correcta se conoce como tiempo de búsqueda. Una vez que la cabeza está en la ubicación espacial concéntrica correcta, se pasa más tiempo esperando que el disco gire, de modo que el sector con los datos solicitados esté debajo de la cabeza. Esta cantidad de tiempo se conoce como latencia.

Las cabezas están colocadas a unos pocos nanómetros de los discos giratorios. Se dice que las cabezas "vuelan" por encima de la fuente y, como tal, la distancia entre la cabeza y la fuente se denomina "altura de vuelo". Los cabezales están diseñados para nunca tocar las ubicaciones de los platos que almacenan datos y están recubiertos magnéticamente. En caso de que la cabeza 'toque hacia abajo' en un disco, tanto la cabeza como los sectores de los discos pueden ser destruidos y provocar la pérdida de datos (de ahí la frase "un fallo del disco duro" o "choque del cabezal").

Los discos duros recuperan y almacenan datos de las aplicaciones a petición de la CPU. Esto se conoce como operaciones de entrada / salida - IO para abreviar. Cuando un programa en ejecución requiere un determinado dato, la CPU envía una instrucción para que los datos se obtengan del disco duro. La lectura de este dato es una operación de entrada (desde la perspectiva de la CPU). Luego, el programa puede realizar un cálculo que cambia los datos y los resultados deben almacenarse de nuevo en el disco duro. La CPU solicita que los datos se escriban de nuevo en la unidad. Este sería un ejemplo de una operación de salida (nuevamente, desde la perspectiva de la CPU).

El rendimiento del disco duro se mide principalmente por dos métricas clave 1) el tiempo de respuesta, que es el tiempo que tarda en completarse una operación de lectura o escritura y 2) IOPS, que es un acrónimo de "Operaciones de entrada / salida por segundo". Como su nombre sugiere, IOPS es una medida de las operaciones máximas de IO en un segundo. El factor principal para lograr el máximo IOPS en el menor tiempo de respuesta es la velocidad de rotación del disco duro medida en revoluciones por minuto (RPM). Las velocidades de rotación comunes son 5,400 RPM, 7,200 RPM, 10,000 RPM y 15,000 RPM (comúnmente señaladas como 5.4K, 7.2K, 10K y 15K). Los discos duros con velocidades de rotación más altas (RPM) tendrán un pase de bienes raíces de mayor capacidad por debajo de las cabezas para las operaciones de IO (lecturas y escrituras). Los discos duros con tasas de rotación de RPM más bajas tendrán latencias mecánicas mucho más altas, ya que pasarán menos bienes raíces debajo de las cabezas.

Una herramienta simple para medir las métricas de rendimiento del disco duro se llama IOMeter (vea el enlace a continuación). El programa es muy ligero y fácil de instalar. Una vez que está en funcionamiento, se pueden ejecutar diferentes variaciones de cargas de trabajo para simular las lecturas y escrituras de datos en el disco. Estos datos se analizan y generan métricas para los tiempos de lectura / escritura, IOPS y otras métricas útiles. Las pruebas se pueden guardar para verificaciones consistentes, y los datos se pueden analizar fácilmente en forma de tabla o gráfico.

Los discos duros tienden a categorizarse por caso de uso (capacidad o rendimiento). Las estaciones de trabajo de PC de uso doméstico y de oficina de uso general tienden a usar discos duros de rotación más lenta (5.4K y 7.2K), lo cual está bien para almacenar imágenes y archivos de oficina. Sin embargo, las grandes bases de datos que admiten transacciones bancarias en línea, por ejemplo, utilizan los discos duros de 10K y 15K RPM, ya que serán componentes de un servidor empresarial o una matriz de almacenamiento. Sin embargo, hay un compromiso entre el rendimiento y la capacidad de un disco duro. Por ejemplo, el disco duro de 15K de mayor capacidad disponible en la actualidad es de solo 600 GB, mientras que el disco duro de mayor capacidad para los 5.4K y 7.2K RPM es de 10 TB. La unidad de 600 GB 15K es capaz de 250 IOPS a 3 ms de tiempo de respuesta (promedios). Mientras que la unidad de 10 TB 7.2K TB no mide IOPS en un tiempo de respuesta dado, ya que no está optimizado ni destinado a los casos de uso centrados en IOPS. También hay otras compensaciones en el precio por GB, la energía consumida y el tamaño (2.5 "frente a 3.5" pulgadas).

Las computadoras almacenan datos y archivos en discos duros para su uso posterior. Debido a que los discos duros tienen partes móviles, lleva mucho más tiempo leer un archivo desde un disco duro que desde la memoria RAM o la memoria caché de la CPU. Puede pensar en un disco duro como un archivador: un lugar para almacenar cosas que no estamos usando en este momento, pero que necesitamos más adelante. No tiene suficiente espacio en su escritorio para todos sus papeles, por lo que guarda cosas que no está usando en este momento en el archivador. Una computadora hace justamente esto. Mantiene los archivos que está usando en este momento en la RAM, y los archivos que pueda necesitar más adelante permanecerán en el disco duro. Aunque la RAM tiene tiempos de acceso y respuesta que son dos órdenes de magnitud más rápidos en comparación con los discos duros, su capacidad típica es 1-2 órdenes de magnitud menos que un disco duro típico. Puede colocar resmas de papel en el archivador, pero solo unas pocas en su escritorio.

Se dice que los datos almacenados en la memoria RAM son fugaces, mientras que los datos escritos en un disco duro son persistentes. Esto significa que si la energía se apaga repentinamente, todos los datos que se encontraban en la RAM se perderán y no estarán allí después de que se restablezca la alimentación y se reinicie la computadora. Sin embargo, los datos que se escribieron en el disco duro estarán allí cuando se restaure la energía. Por esta razón, los sistemas operativos y aplicaciones modernos escriben periódicamente datos de sesión y relacionados con la aplicación que actualmente se encuentran en la memoria RAM en el disco duro. De esta manera, si se corta la alimentación, solo se ingresaron 10 minutos de datos en una hoja de cálculo de nueva creación en la que se trabajó durante las 3 horas anteriores a la interrupción de la alimentación y aún no se guardaron en el disco duro. Estos archivos generalmente se indican con una tilde ~ y se pueden encontrar en un directorio temporal o temporal o posiblemente se encuentran en un 'directorio oculto' cuyos contenidos se conocen como archivos ocultos.

## Unidades de estado sólido (SSD)

Las unidades de estado sólido utilizan circuitos integrados para almacenar datos. Por lo tanto, un SSD no tiene partes móviles como el HDD. Esto los hace menos propensos a los choques físicos, se ejecuta silenciosamente y tiene tiempos de lectura / escritura más rápidos gracias a que no es necesario localizar los datos físicamente.

Los SSD generalmente solo se usan como unidades de arranque o almacenamiento para las aplicaciones más utilizadas en la computadora de una persona. Esto se debe a que, aunque su precio ha disminuido mucho en los últimos años, sigue siendo mucho más caro que un disco duro tradicional. Por lo tanto, los discos duros aún se utilizan para almacenar grandes cantidades de datos como nuestras fotos y videos, o en centros de datos o granjas de servidores.

#### Más información:

*   [Wikipedia - Unidad de disco duro](https://en.wikipedia.org/wiki/Hard_disk_drive)
*   [Wikipedia - Altura de vuelo](https://en.wikipedia.org/wiki/Flying_height)
*   [Wikipedia - Almacenamiento de datos informáticos](https://en.wikipedia.org/wiki/Computer_data_storage)
*   [PCMag - SSD vs. HDD: ¿Cuál es la diferencia?](https://www.pcmag.com/article2/0,2817,2404258,00.asp)
*   [Tendencias digitales - SSD vs. HDD](https://www.digitaltrends.com/computing/solid-state-drives-vs-hard-disk-drives)
*   [Proyecto IOMeter](http://www.iometer.org)