


|  **Requerimento**        |   **Interacción activa**                     |                                                    
|:--|:--|
| **dependencias**                |        
| **Precondición**  | El usuario registrado visualiza las publicaciones de los vendedores. |
|   **Descripción**           | El usuario escribe una serie de caracteres en la publicación; el comentario se sube y termina el proceso.
|**secuencia normal**| **Paso 1:** El usuario visualiza una publicación
|                     | **Paso 2:** El usuario entra a la caja de comentarios
|                     | **Paso 3:** El usuario escribe un comentario
|                     | **Paso 4:** El usuario presiona enviar
|                     | **Paso 5:** El comentario se sube a la caja de comentarios
| **Postcondicion**                     | Los comentarios están sujetos a revisión a causa de un reporte de comentario
| **Flujo alternativo**                                      | **Paso 1:** Un usuario reporta el comentario
|                                       | **Paso 2:** El comentario entra en revisión
|                                       | **Paso 3:** El sistema analiza el comentario
|                                       | **Paso 4:** El sistema detecta un uso de lenguaje inadecuado
|                                       | **Paso 5:** El sistema comienza el proceso de “Reporte de publicación o comentario
-----------------------------------------------------------------------------






|  **Requerimento**        |     **El usuario utiliza el buscador**                   |                                                    
|:--|:--|
| **dependencias**                |        
| **Precondición**  | El usuario busca un producto en específico |
|   **Descripción**           | El usuario accede al buscador, escribe un producto, el sistema analiza entre todas las publicaciones y le arroja el resultado obtenido.
|**secuencia normal**| **Paso 1:** El usuario accede al buscador
|                     | **Paso 2:** El usuario escribe el producto que busca
|                     | **Paso 3:** El sistema va arrojando recomendaciones según lo que vaya escribiendo
|                     | **Paso 4:** El sistema analiza entre sus publicaciones
|                     | **Paso 5:** El sistema arroja los resultados obtenidos
| **Postcondicion**                     | El sistema no cuenta con el producto que el usuario busca
| **Flujo alternativo**                                      | **Paso 1:** El sistema no encuentra el producto deseado
|                                       | **Paso 2:** El sistema arroja un mensaje describiendo la situación
--------------------------------------------------------------------------

--------------------------------------------------------------------------
|  **Requerimento**        |     **Comunicación por mensajeria instantanea**                   |                                                    
|:--|--:|
| **dependencias**                |Publicación de productos        
| **Precondición**  | El usuario cliente está interesado en establecer o mantener comunicación directa con un usuario vendedor, que ha visto en las publicaciones de productos. |
|   **Descripción**           | El caso de uso comunicación por mensajería instantánea ocurre cuando dos usuarios de la aplicación (cliente y vendedor) se contactan de forma privada en la aplicación para concretar una compra o venta.
|**secuencia normal**| **Paso 1:** El usuario cliente selecciona el perfil de un vendedor de un producto que le ha interesado
|                     | **Paso 2:** En el perfil selecciona la función de enviar mensaje.
|                     | **Paso 3:** Redacta uno o más mensajes y los envía.
|                     | **Paso 4:** Si el vendedor desea sostener la conversación, le responde al cliente. La comunicación puede continuar ilimitadamente.
| **Postcondicion**                     | La función ayuda a que los usuarios se puedan poner de acuerdo para una transacción presencial, si ambos lo desean.
| **Flujo alternativo**                                      | **Paso 1:** Alguno de los implicados no desea establecer o continuar la comunicación con el otro.
|                                       | **Paso 1.1:** Ignora los mensajes del otro y/o elimina el chat
|                                       | **Paso 2:** Alguno de los usuarios resulta molesto/desagradable y se desea eliminar la posibilidad de que envíe mensajes.
|                                       | **Paso 2.1:** Caso de uso bloqueo de usuario.
|                                       | **Paso 3:** Se ha recibido un bloqueo de usuario
|                                       | **Paso 3.1:** La aplicación no permite redactar y enviar un mensaje.
--------------------------------------------------------------------------


--------------------------------------------------------------------------
|  **Requerimento**        |     **Bloqueo de usuario**                   |                                                    
|:--|--:|
| **dependencias**                | Comunicación por mensajería instantánea       
| **Precondición**  | A un usuario, otro usuario, (con el cual probablemente ,aunque no obligatoriamente ya ha tenido alguna interacción por mensajería), le parece molesto/desagradable. |
|   **Descripción**           | El caso de uso ocurre cuando un usuario desea eliminar la posibilidad de que el caso de uso comunicación por mensajería instantánea se dé con otro usuario en específico.
|**secuencia normal**| **Paso 1:** El usuario ingresa en el chat del que desea bloquea
|                     | **Paso 2:** Selecciona bloquear usuario
|                     | **Paso 3:** Redacta con menos de 200 caracteres por qué desea bloquear al otro
|                     | **Paso 4:** Da por confirmado el bloqueo  
| **Postcondicion**                     | Ambos implicados ya no pueden escribirse, ni enviarse mensajes.
---------------------------------------------------------------------------


--------------------------------------------------------------------------
|  **Requerimento**        |     **Desbloqueo al usuario**                   |                                                    
|:--|--:|
| **dependencias**         | Comunicación por mensajería instantánea / Bloqueo de usuario      
| **Precondición**         |Un usuario tiene que haber sido bloqueado por otro. |
|   **Descripción**        | Un usuario desea revertir el bloqueo que le ha aplicado a otro.
|**secuencia normal**      | **Paso 1:** El usuario ingresa al chat del bloqueado.
|                          | **Paso 2:** Selecciona la opción desbloquear. 
| **Postcondicion**        | Ambos usuarios ya pueden enviarse mensajes
| **Excepciones**          | Si dos usuarios se han bloqueado mutuamente, el que solamente uno desbloquee a otro no permite la postcondición.
---------------------------------------------------------------------------


--------------------------------------------------------------------------
|  **Requerimento**        |     **Reporte de publicacion o comentario**                   |                                                  
|:--|--:|
| **dependencias**                | Un usuario tiene acceso a las publicaciones de los vendedores y a los comentarios publicados en ellos.       
| **Precondición**  |A un usuario una publicación o comentario le parece inadecuado o engañoso y decide reportarlo a la moderación para su eliminación |
|   **Descripción**           | Un usuario desea revertir el bloqueo que le ha aplicado a otro.
|**secuencia normal**| **Paso 1:** Un usuario se encuentra con una publicación o comentario que considera inadecuado o engañoso.
|                     | **Paso 2:** Selecciona la opción reportar.
|                     | **Paso 3:* Explica con menos de 200 caracteres el por qué la publicación o el comentario le parece inadecuado o engañoso.
|                     | **Paso 4:** Confirma el reporte.
| **Postcondicion**                   | La moderación evaluará el tipo de acción y de sanción que tomará, que puede consistir en: ninguna, una llamada de atención y la eliminación de la publicación o comentario, y la eliminación del usuario reportado de la plataforma.
| **Excepciones**                     | **Paso 1:** El usuario ya ha reportado la misma publicación anteriormente.
|                                     | **Paso 2:** Se le avisa que no puede volver a reportar la misma publicación.
---------------------------------------------------------------------------

--------------------------------------------------------------------------
|  **Requerimento**        |     **Publicación de productos**                        |                                                  
|:--|--:|
| **dependencias**         | Gestion de usuarios       
| **Precondición**         |El usuario debe estar registrado en la app como vendedor |
|   **Descripción**        | El usuario vendedor decide distribuir un producto, por lo que lo pública y describe su artículo
|**secuencia normal**      | **Paso 1:** El usuario vendedor selecciona el producto que decida vender
|                          | **Paso 2:** Añade las imágenes que publicará
|                          | **Paso 3:** Añade una descripción de su producto
|                          | **Paso 4:** Añade información de usuario
| **Postcondicion**        | La publicación se verá reflejada en el feed de los usuarios
| **Excepciones**          | **Paso 1:** El usuario vendedor decide borrar su publicación
|                          | **Paso 2:** Se le acabó un artículo de venta, por lo que decidió borrar la publicación
---------------------------------------------------------------------------


--------------------------------------------------------------------------
|  **Requerimento**        |     **Reaccion a usuario, publicacion o comentario**                   |                                                    
|:--|--:|
| **dependencias**                |  Gestión de usuarios / Publicación de producto     
| **Precondición**  | El usuario entró a la publicación de un producto |
|   **Descripción**           | Esta funcionalidad le permitirá poder dar su opinión respecto a un comentario, al perfil de un usuario a un producto
|**secuencia normal**| **Paso 1:** El usuario visualiza una publicación de un producto
|                     | **Paso 2:** Analiza el contenido de la publicación
|                     | **Paso 3:** Tiene la posibilidad de reaccionar al usuario, a la publicación o un comentario
| **Postcondicion**                     | Estas funciones ayudan a atraer al usuario comprador al producto, a adquirirlo y que el vendedor pueda distribuir su producto
| **Excepciones**                     | **Paso 1:** Reacciona de manera positiva a un usuario, a la publicación o un comentario
|                                     | **Paso 1.1:** E1.  El usuario comprador le da un like a un comentario
|                                     | **Paso 2:** Reacciona de manera negativa a un usuario, a la publicación o un comentario
|                                     | **Paso 2.1:** El usuario comprador le da un dislike a un comentario
---------------------------------------------------------------------------

--------------------------------------------------------------------------
|  **Requerimento**        |     **Gestion de usuarios**                   |                                                    
|:--|--:|
| **dependencias**                |      Protección de datos 
| **Precondición**  | El usuario debe ser estudiante de la Universidad Autónoma de Yucatán (UADY) |
|   **Descripción**           | Registro de Usuario: Permite a un nuevo usuario crear una cuenta en el sistema proporcionando información como nombre, correo electrónico y contraseña.
|**secuencia normal**| **Paso 1:** El usuario solicita el acceso a crear un perfil de usuario
|                     | **Paso 2:** El sistema solicita la información sobre: ¿Usuario vendedor o usuario consumidor?
|                     | **Paso 3:** El usuario ingresa su correo institucional como parte del registro
|                     | **Paso 4:** El usuario crea su contraseña
| **Postcondicion**                     | Permite a los usuarios tener un perfil dentro del sistema, ya sea entrar como usuario vendedor o como usuario consumidor.
| **Excepciones**                     | **Paso 1:** En caso de no contar con un correo institucional, permitir el uso de otro correo electrónico no necesariamente institucional
|                                     | **Paso 2:** Ingresar correo electrónico y contraseña para el registro de usuario
---------------------------------------------------------------------------



--------------------------------------------------------------------------
|  **Requerimento**        |     **Mejoras de accesibilidad**                   |                                                    
|:--|--:|
| **dependencias**                |  Publicación de productos / Organización de publicaciones     
| **Precondición**  | El usuario necesariamente necesita tener su perfil de usuario creado. |
|   **Descripción**           | Ajuste de Texto: Permitir a los usuarios ajustar el tamaño del texto según sus necesidades para mejorar la legibilidad
|**secuencia normal**| **Paso 1:** El usuario inicia sesión dentro del programa
|                     | **Paso 2:** El usuario se dirige al apartado de ajustes.
|                     | **Paso 3:** El sistema proyecta una interfaz en la que aparecen varias opciones.
|                     | **Paso 4:** El usuario accede a la opción de “Mejoras de accesibilidad”
|                     | **Paso 5:** El usuario se dirige a “Ajustes de Texto”
|                     | **Paso 6:** El usuario ajusta el tamaño del texto según sus necesidades para mejorar la legibilidad.
| **Postcondicion**                   | El usuario podrá tener una mejora visual
| **Excepciones**                     | **Paso 1:** El usuario ingresa al sistema.
|                                     | **Paso 2:** El usuario se dirige al apartado de ajustes
|                                     | **Paso 3:** El usuario accede a la opción de “refresh”
|                                     | **Paso 4:** El sistema se actualiza automáticamente
---------------------------------------------------------------------------


--------------------------------------------------------------------------
|  **Requerimento**        |     **Edición de perfil**                   |                                                    
|:--|--:|
| **dependencias**                |  Gestión de usuarios / Base de datos     
| **Precondición**  | El usuario tendrá la posibilidad de cambiar en su perfil de la app sus datos personales, de contacto, etc. |
|   **Descripción**           | El sistema deberá permitir ingresar nuevos datos y guardarlos para actualizar la información del usuario.
|**secuencia normal** | **Paso 1:** Al entrar a su perfil en la parte inferior de su nombre de usuario habrá un botón de “Editar Perfil” que deberá apretar.
|                     | **Paso 2:** Al dar click le aparecerán varios apartados con sus datos (correo, teléfono, contraseña,nombre de usuario, descripción y foto de perfil) 
|                     | **Paso 3:** Al lado de cada uno habrá un icono de más que servirá para corregir y/o cambiar los datos
|                     | **Paso 4:** El usuario ingresará los datos nuevos
|                     | **Paso 5:** Debajo de cada  espacio para modificar los datos se mostrará una opción en la cuál el usuario decidirá si desea que su información se pública o privada.
|                     | **Paso 6:** Al terminar en la esquina superior izquierda le aparecerá el botón de guardar y le dará click.
|                     | **Paso 7:** El sistema lo llevará a su perfil donde se verán reflejados los cambios realizados. 
| **Postcondicion**                   | El usuario podrá ver la información que eligió visible en su perfil.
| **Excepciones**                     | **Paso 1:** Al usuario le aparecerá su foto de perfil con un icono de más en la esquina inferior derecha
|                                     | **Paso 1.1:** Le dará click y aparecerá la opción de subir la foto
|                                     | **Paso 1.3:** Seleccionará la que le guste y le dará en el botón de “Seleccionar” en la parte superior derecha.
|                                     | **Paso 1.4:** Lo devolverá a la página de cambios.
---------------------------------------------------------------------------
