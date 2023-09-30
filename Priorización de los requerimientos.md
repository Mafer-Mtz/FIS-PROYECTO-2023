# Priorización de los requerimientos
---
Definidas las listas de requerimientos, nos valemos de algunos métodos para definir su importancia. Desde luego que todos los requerimientos tienen alguna (por algo están incluidos en las listas), sin embargo, consideramos vital identificar cuáles son prioritarios, y cuales, en diferente medida, lo son menos, ya que notamos que hay algunos desafíos por sortear, como posibles costos, falta de tiempo o desafíos técnicos muy complejos, que tal vez no nos sea factible cumplir con todos los requisitos. Por tanto, paso a paso cumpliremos los requerimientos más importantes, y posteriormente, pasaremos a los demás. (de acuerdo con la metodología elegida de desarrollo de software)
Hemos escogido 3 métodos de priorización de requerimientos. Generalmente con una es suficiente, pero hemos elegido varios para contrastar resultados. A continuación, los nombramos y explicamos:
Votación: Asigna el número mayor al requerimiento más importante, y continúa en orden descendente con los siguientes en importancia, de tal forma que el menos importante recibe el número menor.  
Moscow: Clasifica a los requerimientos en 4 categorías:
    Must: obligatorio
    should: de alta prioridad
    could: preferido, pero no necesario
    would: puede ser pospuesto y sugerido para futura ejecución
Cinco “porques”: Se argumenta el por qué de cada requerimiento, y a su vez, se prosigue con la argumentación del “por qué del por qué”. El nombre del método indica que se hace cinco veces, aunque esto no es obligatorio.

Requerimientos funcionales
| -- | -------- | -------- |
|Requisito|Votación|Moscow|Cinco “porques”|
|Registro de nuevos usuarios y permitir el acceso a usuarios ya registrados|4|Must|-Porque los usuarios necesitan tener una identidad. -Porque necesitan ser identificados por otros usuarios, especialmente en el vínculo comprador-vendedor.|
|Facilitar la comunicación en tiempo real a través de un sistema de chat en tiempo real con el vendedor|3|Could|-Porque los compradores y vendedores necesitan comunicarse entre sí. -Porque necesitan concretar el lugar y hora de la compra/venta|
|Permitir la modificación de usuarios, así como la confirmación de datos de contacto (correo, número de teléfono, etc.)|2|Could|-Porque así se crea una reputación acerca de los vendedores. -Porque da información acerca de qué tan confiable es un vendedor. -Porque se debe promover que los buenos vendedores tengan visibilidad en la plataforma.-Porque esto hace útil a la aplicación como fuente de referencia.|
|Posibilidad de agregar fotos, descripciones y precios del producto que se busque vender|5|Must|-Porque es necesario tanto conocer lo que posiblemente se compre, como exhibir un producto a vender. -Porque es la forma en que alguien se puede interesar en adquirir un producto. -Porque de esta forma la plataforma se vuelve útil para compra y venta.-Porque así es como los usuarios pueden tener interés en usarla.|

Requisitos no funcionales
| -- | -------- | -------- |
|Requisito|Votación|Moscow|Cinco “porques”|
|Mejoras de accesibilidad|4|Could| |
|Exclusividad universitaria|5|Would|-Porque los usuarios prefieren ver publicaciones específicas a sus necesidades. -Porque así ahorran tiempo.|
|Supervisión de productos ilícitos|3|Should|-Porque los desarrolladores quieren evitar que su producto se vea inmiscuido en cualquier actividad ilegal. -Porque puede crear problemas legales y de seguridad en desarrolladores y usuarios.|
|Protección de datos|1|Must|-Porque la información personal debe ser confidencial. -Porque de no ser así se pone en peligro la integridad de los usuarios.|
|Actualización constante de la página|2|Must|-Porque la plataforma debe mantenerse vigente. -Porque la información que contiene debe ser útil en el momento que se visualiza.|
