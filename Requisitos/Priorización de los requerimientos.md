# Priorización de los requerimientos
---
Definidas las listas de requerimientos, nos valemos de algunos métodos para definir su importancia. Desde luego que todos los requerimientos tienen alguna (por algo están incluidos en las listas), sin embargo, consideramos vital identificar cuáles son prioritarios, y cuales, en diferente medida, lo son menos, ya que notamos que hay algunos desafíos por sortear, como posibles costos, falta de tiempo o desafíos técnicos muy complejos, que tal vez no nos sea factible cumplir con todos los requisitos. Por tanto, paso a paso cumpliremos los requerimientos más importantes, y posteriormente, pasaremos a los demás. (de acuerdo con la metodología elegida de desarrollo de software)
Hemos escogido 3 métodos de priorización de requerimientos. Generalmente con una es suficiente, pero hemos elegido varios para contrastar resultados. A continuación, los nombramos y explicamos:
- **Votación:** Asigna el número mayor al requerimiento más importante, y continúa en orden descendente con los siguientes en importancia, de tal forma que el menos importante recibe el número menor.  
- **Moscow:** Clasifica a los requerimientos en 4 categorías:
    - **Must:** obligatorio
    - **should:** de alta prioridad
    - **could:** preferido, pero no necesario
    - **would:** puede ser pospuesto y sugerido para futura ejecución
- **Cinco “porques”:** Se argumenta el por qué de cada requerimiento, y a su vez, se prosigue con la argumentación del “por qué del por qué”. El nombre del método indica que se hace cinco veces, aunque esto no es obligatorio.

## Requerimientos funcionales

| Requisito | Votación | Moscow | Cinco “porques” |
| -------- |  :---: |  :---: | -------- |
| Manejo de usuarios: Registro de nuevos usuarios y permitir el acceso a usuarios ya registrados | 5 | Must | <ul><li>Porque los usuarios necesitan tener una identidad.</li><li>Porque necesitan ser identificados por otros usuarios, especialmente en el vínculo comprador-vendedor. |
| Comunicación: Facilitar la comunicación en tiempo real a través de un sistema de chat en tiempo real con el vendedor | 1 | Would |<ul><li>Porque los compradores y vendedores necesitan comunicarse entre sí. </li><li>Porque necesitan concretar el lugar y hora de la compra/venta |
| Retroalimentación activa: Permitir a los usuarios calificarse entre sí y dejar reseñas sobre productos adquiridos | 2 | Could |<ul><li>Porque la información en cuanto a la calidad de las ofertas y confiabilidad de los vendedores ayuda al usuario a decidir|
| Publicaciones: Posibilidad de subir fotos, descripciones y precios del producto que se busque vender.| 6 | Must |<ul><li>Porque es necesario conocer lo que posiblemente se compre, así como tener un medio para publicitar un producto </li><li>Porque es la forma en que alguien se puede interesar en adquirir un producto. </li><li>Porque de esta forma la plataforma se vuelve útil para compra y venta. </li><li>Porque así es como las personas pueden llegar a tener interés en usarla. |
| Organización de publicaciones: Manejo de organización de publicaciones de acuerdo a relevancia de productos. | 3 | Should |<ul><li>Porque los usuarios prefieren ver publicaciones actuales y que le hayan sido útiles a otros.</li><li>Porque así ahorran tiempo y mejoran sus posibilidades de hacer una buena compra. |
| Compatibilidad: Tipo de dispositivos compatibles de acuerdo a nuestra aplicación siendo en este caso para dispositivos móviles. | 4 | Should | <ul><li>Porque son el tipo de dispositivo ideal para búsquedas, en cualquier momento.</li><li>Porque los teléfonos celulares son muy utilizados, las personas los llevan a todos lados. </li><li>Porque esto es fundamental, ya que necesitamos que la aplicación esté a la mano de los usuarios. |


## Requerimientos no funcionales

| Requisito | Votación | Moscow | Cinco “porques” |
| -------- |  :---: |  :---: | -------- |
| Mejoras de accesibilidad | 2 | Should | <ul><li>Porque la información en cuanto a la calidad de las ofertas y confiabilidad de los vendedores ayuda al usuario a decidir  |
| Supervisión de productos ilícitos | 3 | Should| <ul><li>Porque los desarrolladores quieren evitar que su producto se vea inmiscuido en cualquier actividad ilegal. </li><li>Porque puede crear problemas legales y de seguridad en desarrolladores y usuarios. |
| Protección de datos | 5 | Must | <ul><li>Porque la información personal debe ser confidencial. </li><li>Porque de no ser así se pone en peligro la integridad de los usuarios. |
| Actualización constante de la página | 4 | Must | <ul><li>Porque la plataforma debe mantenerse vigente. </li><li>Porque la información que contiene debe ser útil en el momento que se visualiza. |
| Moderación del lenguaje en las reseñas | 1 | Could | <ul><li>Porque se debe fomentar un ambiente de cordialidad y respeto.</li><li>Porque de no ser así el contenido de la plataforma puede volverse ofensivo. |
