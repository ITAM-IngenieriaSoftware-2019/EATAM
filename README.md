# EATAM
Proyecto final equipo Los Tecolotes (la comida)

Integrantes:
- Amanda Velasco Gallardo             154415
- Tábata Ailé González Alvarado       155999
- Víctor Hugo Flores Pineda           155990
- Juan José López Jaramillo           155903

# Tabla de contenido
1. System Requirements
    1. Introduction
        1. Purpose
        2. Document conventions
        3. Intended Audience and Reading Suggestions
        4. Product Scope
        5. References
    2. Overall Description
        1. Product perspective
        2. Product Functions
        3. User Classes and Characteristics
        4. Operating Environment
        5. Design and Implementation Constraints
        6. User Documentation
        7. Assumptions and Dependencies
    3. External Interface Requirements
        1. User Interfaces
        2. Hardware Interfaces
        3. Software Interfaces
        4. Communication Interfaces
    4. System Features
        1. Entrada al sistema con credenciales de usuario
        2. Registro de nuevo usuario
        3. Configuraciones de la cuenta del usuario
        4. Visualización del menú Comensal
        5. Métodos de pago del Comensal
        6. Petición de pedido
        7. Notificación de pedido entregado
        8. Pantalla de perfil del Comensal
        9. Menú para navegar por las funcionalidades del Repartidor
        10. Perfil del usuario y activación del modo Repartidor
        11. Información del pedido en curso que el usuario Repartidor está completando
        12. Modificación de métodos en que el usuario Repartidor recibe sus pagos
        13. FAQs y contacto a soporte para el usuario Repartidor
        14. Notificaciones de pedidos entrantes
    5. Other Nonfunctional Requirements
        1. Performance Requirements
        2. Safety Requirements
        3. Security Requirements
        4. Software Quality Attributes
        5. Business Rules
2. Plan de calidad
    1. Test Plan Identifier
    2. References
    3. Introduction
    4. Test Items
    5. Software Risk Issues
    6. Features to be Tested
    7. Features not to be Tested
    8. Approach
    9. Item Pass/Fail Criteria
    10. Suspension Criteria and Resumption Requirements
    11. Test Deliverables
    12. Remaining Test Tasks
    13. Environmental Needs
    14. Staffing and Training Needs
    15. Responsibilities
    16. Schedule
    17. Planning Risks and Contingencies
    18. Approvals
    19. Glossary
3. Arquitectura
4. Metodología
5. Documentación para replicar

# System Requirements
## 1. Introduction 
### 1.1 Purpose 
EATAM es un sistema de gig economy para los alumnos, profesores y personal que forman parte del Instituto Tecnológico Autónomo de México. En este sistema podrán pedir o entregar comida a quien lo solicite dentro de las instalaciones de la institución. La finalidad de este producto es que los usuarios puedan pedir comida y/o ganar dinero extra en su tiempo libre. 
### 1.2 Document Conventions
El documento se basa en la jerarquía especificada por la IEEE. Las prioridades fueron definidas dependiendo de la importancia de funcionalidad del feature. Para la estimación se utilizó una escala extremadamente sencilla, la cual incluye las prioridades baja, media y alta.
A lo largo del documento se presentará un elemento característico que ronda en torno al propósito descrito anteriormente, se presentará la descripción de las dos secciones incluídas en EATAM: Comensal y Repartidor. Este documento abarcará la descripción de cada sección de manera individual, siempre y cuando el apartado involucre alguna descripción de las funcionalidades de la aplicación.

### 1.3 Intended Audience and Reading Suggestions
El documento está planeado para ser leído por desarrolladores, esto con la intención de poder ser mejorado y actualizado en el futuro. Por lo tanto, en el documento se expondrán los detalles técnicos necesarios del sistema. Se recomienda que la lectura de este sea en orden cronólogico. Además, se podrán encontrar referencias para el conocimiento y desarrollo de partes específicas del sistema. 
### 1.4 Product Scope 
El objetivo de este sistema se divide en dos. El primero es el de facilitar al usuario comensal la acción de ir por alimentos hasta su establecimiento deseado. El segundo objetivo es para el usuario repartidor y es poder recibir un ingreso en su tiempo libre en la institución. 
### 1.5 References
El sistema se creó utilizando [Just in mind prototyper](https://www.justinmind.com/), que es una plataforma para realizar propototipos de aplicaciones para diferentes positivos. 
Los íconos que se utilizaron para la elaboración de la aplicación se obtuvieron de: 
  - [FontAwesome](https://fontawesome.com/)
  - [Flaticon](https://www.flaticon.com/home)

## 2. Overall Description 
### 2.1 Product Perspective
Esta versión es la primera del sistema y este surge tras analizar la necesidades de la comunidad. Muchas veces, por estar trabajando en cosas personales o de la institución, la comunidad prefiere continuar con sus deberes que comer. Además, este sistema crea una oportunidad de trabajo flexible. Por lo tanto, se busca satisfacer dos necesidades de la comunidad y que sea la comunidad la que las satisfaga. 
### 2.2 Product Functions 
Como ya se ha hecho hincapié anteriormente, el sistema se puede dividir en dos entidades. Por lo mismo, las funciones del sistema se dividen en dos. 

Funciones para el comensal: 
 - Petición pedido:  el usuario agrega al carrito el producto que desea consumir. Posteriormente, el usuario debe indicar dónde quiere que se le haga la entrega y confirma el pedido pagando. 
 - Notificación de pedido entregado: el usuario debe confirmar que el pedido le fue entregado correctamente. 

Funciones para el repartidor: 
  - Modo repartidor: el usuario podrá definir si desea estar activo como repartidor. En caso de estar activo cuando se haga una petición de orden podrá recibirla y hacer lo necesario para que el comensal reciba su pedido. 
  - Recoger y entregar la orden: el usuario podrá aceptar o rechazar una orden. Si el usuario la acepta, se despliega la información sobre la orden, por ejemplo, dónde tiene que recogerla, los productos que tiene que recoger, a dónde la tiene que llevar y la información sobre el comensal que hizo la orden. 
### 2.3 User Classes and Characteristics
Los usuarios que interactuarán con la aplicación son: 
  - Estudiantes: todo individuo que esté tomando clases en la institución, ya sea licenciatura, maestría, doctorado, diplomado, etc. 
  - Profesores: todos los catedráticos de la institución.
  - Personal adicional: todo aquella persona que su trabajo consista en prestar un servicio a la institutición. El personal adcional esta formado por secretarias, mantenimiento, limpieza, administrativos, personal del restaurante y estacionamiento, etc.

Los usuarios tendrán gran habilidad para identificar y conocer el uso de la aplicación debido a que existen más aplicaciones con el mismo concepto, además el ITAM se caracteriza por brindar un pensamiento crítico y analítico, por lo que utilizarán la aplicación de manera sencilla e intuitiva sin ningún tipo de dificultad.
### 2.4 Operating Environment 
Por restricciones definidas por **Just in mind**, que es que se trabaja sobre la pantalla de un dispositivo en específico y para replicar a otros hay que ajustarlo manualmente, el sistema está hecho para trabajar solamente en la pantalla de un iPhone X. Por lo mismo, las llamadas a los usuarios solo corresponden a las pantallas establecidas por el sistema operativo iOS y excluyen a las de Android. 
### 2.5 Design and Implementation Constraints
Durante el semestre y horas del día, el sistema tendrá una demanda distinta. Por ejemplo, en finales y antes de los exámenes de economía, habrá más demanda por parte de los comensales debido a que muchos estudiantes preferirán que la comida se les lleve al lugar de estudio en vez de ellos salir por ella. Además, se debe tomar en consideración las áreas en que está prohibido introducir comida, por ejemplo, la biblioteca. Asimismo, se debe considerar que es necesario especificar las restricciones para la entrega de comida, con tal de no interrumpir una clase para hacer la entrega. 
### 2.6 User Documentation 
La documentación necesaria para el desarrollo de este producto se puede encontrar en el punto 1.5, donde se especifican las URLs de las herramientas que se utilizaron para elaborar la aplicación. Asimismo, se recomienda utilizar otras plataformas como [YouTube ](https://www.youtube.com/?hl=es-419&gl=MX)para ver tutoriales donde se especifique paso a paso cómo crear ciertos elementos en la aplicación. 
### 2.7 Assumptions and Dependencies
El sistema depende de la autorización del Instituto Tecnológico Autonomo de México de poder hacer la recepción y entrega del pedido dentro de las instalaciones, además de que los restaurantes y locales a los alrededores de la institución estén dispuestos a ser parte de EATAM.
La aplicación depende de que el usuario tenga un dispositivo móvil y que tenga un conocimiento de nivel medio del uso del mismo. Asume que las personas que integran la institución tienen tarjeta de crédito y/o débito, que la persona que reparte el pedido es realmente la persona registrada en la aplicación y que la persona que realiza una petición brindas su ubicación de manera verídica.

## 3. External Interface Requirements
### 3.1 User Interfaces
- ConfRelacionITAM: Esta pantalla muestra opciones para indicar qué relación tiene el usuario con el ITAM y en caso de que sea estudiante solicita indicar en qué semestre se encuentra, además contiene un botón que actualiza esta información. También contiene un mensaje de error en caso de que no se haya seleccionado un semestre.
- ConfNombre: Esta pantalla muestra un campo para indicar el nombre del usuario, además contiene un botón que actualiza esta información.
- ConfPassword: Esta pantalla muestra un campo para indicar una contraseña, además contiene un botón que actualiza esta información.
- ConfEmail: Esta pantalla muestra un campo para indicar el correo electrónico del usuario, además contiene un botón que actualiza esta información. También contiene un mensaje de error que aparece cuando el correo solicitado no tiene el dominio @itam.mx
- ConfTelefono: Esta pantalla muestra un campo para indicar el número telefónico del usuario, además contiene un botón que actualiza esta información.
- ConfApellido: Esta pantalla muestra un campo para indicar el apellido del usaurio, además contiene un botón que actualiza esta información.
- ConfFoto: Esta pantalla muestra el carrete del usuario para que elija una foto de perfil, contiene un botón para agregarla y uno para eliminarla de la selección.
- Configuracion: Esta pantalla muestra el nombre, apellido, número de teléfono, correo, contraseña, foto y relación con el ITAM y te permite dar clic en cada opción para modificar la información agregada.
- HomePage: Esta pantalla muestra el ícono de Comensal y el de Repartidor como botones. 
- Registro: Esta pantalla muestra campos de texto: Usuario, email, contraseña y confirmar contraseña, estos se llenan para registrar al usuario, además tiene un botón que confirma el registro.
- Apple ID Login: Esta pantalla muestra los siguientes campos de texto: Email y Password, arroja un error si el usuario no está registrado en la aplicación y contiene dos botones: el primero para iniciar sesión y el segundo para registrarse.
- Loading screen: Esta pantalla es la principal/inicial y muestra el Logo de la aplicación.
- RepartidorHP: Esta pantalla representa el menú principal de la sección de Repartidor. Muestra la imagen del repartidor, la información general en un recuadro (nombre, relación con el ITAM, antigüedad, total de pedidos y calificación promedio); un recuadro con una gráfica indicando los ingresos semanales; un recuadro que indica una estadística de los lugares en los que llegan más pedidos y una opción para activar el modo repartidor.
Si el modo repartidor está activo, en esta pantalla aparece la notificación de que un pedido ha sido registrado y brinda la opción con los botones de Rechazar o Aceptar; si el usuario da clic en Aceptar, arroja a otra pantalla, si da clic en Rechazar, arroja un mensaje advirtiendo que la calificación del repartidor será modificada.
Además, esta pantalla tiene un botón en la parte superior izquierda que muestra un menú; este menú contiene los siguientes botones  direccionadores: Mi Perfil, Orden en curso, Métodos de Pago, Centro de Ayuda, Configuración y Cambiar Modo, todos estos envían a otras pantallas. 
- RepartidorMetodosPago: Esta pantalla muestra las tarjetas registradas en la aplicación, además botones que te permite agregar o eliminar alguna tarjeta.
- RepartidorNuevoMetodoPago:Esta pantalla muestra campos de texto: Número de tarjeta, Fecha de vencimiento y código de seguridad. Arroja un error en caso de que la tarjeta no sea válida y tiene un botón para continuar con el registro de la tarjeta.
- RepartidorOrden:Esta pantalla muestra la información del pedido y del cliente al que será entregado el mismo, contiene un botón que permite llamar al comensal y los siguiente botones adicionales: Finalizar y Cancelar. Si el usuario da clic en el botón de Finalizar, la aplicación envía un recuadro que permite calificar al comensal, si elige Cancelar, arroja un mensaje que indica que al cancelar el repartidor puede ser penalizado y en el mismo mensaje muestra dos botones: Aceptar y Rechazar.
- RepartidorAyuda: Esta pantalla muestra algunas preguntas frecuetes de los comensales con los siguientes recuadros direccionadores: No he recibido mi pago, No funciona el código de pago, Llamar a un asistente, Mandar mensaje a un asistente y Ver mis mensajes con soporte.
- RepartidorTelefono: Esta pantalla muestra la llamada al soporte de la aplicación.
- RepartidorFotoCliente: Esta pantalla muestra la fotografía del comensal.
- RepartidorCodigoPago: Esta pantalla muestra un código QR.
- Pago: Esta pantalla muestra en un párrafo las razones por las que el repartidor no ha recibido su pago y muestra dos botones: un ícono de cara feliz y uno de cara triste.
- Codigo: Esta pantalla muestra en un párrafo las razones por las no ha funcionado el código de pago y muestra dos botones: un ícono de cara feliz y uno de cara triste.
- Convo: Esta pantalla muestra un chat y un cuadro de texto con un botón que te permite escribir un mensaje y enviarlo.
- ComensalHP: Esta pantalla muestra un botón en la parte superior izquierda que te direcciona a otra pantalla; muestra un campo de búsqueda y muestra recuadros direccionadores que contienen elementos que forman parte del menú de la aplicación.
- MenuComensal: Esta pantalla muestra un menú; este menú contiene los siguientes botones  direccionadores: Datos de Perfil, Centro de Ayuda, Historial de pedidos, Métodos de pago, Configuración y Cambiar Modo, todos estos envían a otras pantallas.
- histPedidos: Esta pantalla muestra el historial de los pedidos con la siguiente información: Fecha, Ubicación y Total pagado, además contiene una scrollbar para poder moverse y visualizar todos los pedidos.
- ayudaComensal: Esta pantalla muestra la llamada con el comensal.
- comensalMetodosPago: Esta pantalla muestra las tarjetas registradas en la aplicación, además botones que permiten agregar o eliminar alguna tarjeta.
- ChilaquilesPollo: Esta pantalla muestra la imagen de un platillo; opciones para añadir elementos al platillo que pueden ser seleccionadas por medio de radiobuttons; un cuadro de texto para agregar comentarios; un ícono de + y uno de - para agregar o quitar 1 unidad del platillo y un botón para continuar.
- datosPerfilComensal: Esta pantalla muestra la información del comensal: Foto, Nombre, Usuario, Total de pedidos y Calificación promedio.
- ComensalHP2: Esta pantalla muestra los mismos elementos que la pantalla "ComensalHP" y además un botón en la parte inferior que muestra el total a pagar y permite continuar con el pedido.
- Ubicacion: Esta pantalla muestra botones direccionadores dependiendo de la zona general en la que se encuentra el usuario.
- Ubicacion2: Esta pantalla muestra botones que permiten especificar de manera detallada dónde se encuentra e usuario.
- infoConfirm: Esta pantalla muestra la información de la ubicación del usuario; una lista desplegable para elegir tarjeta de crédito o débito; cuadros de texto para colocar: número de tarjeta, fecha de vencimiento y código de seguridad; un mensaje con el total a pagar y un botón para proceder con el pago.
- esperaEntrega: Esta pantalla muestra la siguiente información del repartidor: Foto, Nombre, Número de entregas.
- esperaEntrega2: Esta pantalla muestra lo mismo que la pantalla "esperaEntrega" y un botón que permite al usuario confirmar el pedido.
- Valoracion: Esta pantalla muestra una radio list con opciones para calificar al repartidor y un botón que permite al usuario finalizar el pedido.
### 3.2 Hardware Interfaces
La aplicación funciona en dispositivos iPhone X que deben tener por lo menos un sistema operativo iOS 11.
### 3.3 Software Interfaces
La aplicación requiere obligatoriamente un sistema operativo mayor a iOS 11, utiliza servicios de los bancos para realizar transacciones, tiene contacto con información clasificada del ITAM como: especificaciones de ubicación y datos de personas relacionadas con la institución. Necesita de Wi-fi.
### 3.4 Communication Interfaces
EATAM cuenta con un servidor que permite la vinculación del repartidor con el comensal; contiene comunicaciones con el sistema de correos del ITAM y con su tabla de usuarios; además, maneja comunicaciones con los servidores de los bancos para realizar transacciones.
## 4. System Features

**Features comunes a todos los usuarios**
### 4.1 [Entrada al sistema con credenciales de usuario](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/1)
### 4.2 [Registro de nuevo usuario](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/5)
### 4.3 [Configuraciones de la cuenta del usuario](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/9)

**Features del modo Comensal**
### 4.4 [Visualización del menú Comensal](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/16)
### 4.5 [Métodos de pago del Comensal](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/17)
### 4.6 [Petición de pedido](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/18)
### 4.7 [Notificación de pedido entregado](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/19)
### 4.8 [Pantalla de perfil del Comensal](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/20) 

**Features del modo Repartidor**
### 4.9 [Menú para navegar por las funcionalidades del Repartidor](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/6)
### 4.10 [Perfil del usuario y activación del modo Repartidor](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/13)
### 4.11 [Información del pedido en curso que el usuario Repartidor está completando](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/8)
### 4.12 [Modificación de métodos en que el usuario Repartidor recibe sus pagos](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/12)
### 4.13 [FAQs y contacto a soporte para el usuario Repartidor](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/11)
### 4.14 [Notificaciones de pedidos entrantes](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/7)

## 5. Other Nonfunctional Requirements
### 5.1 Performance Requirements
Es necesario considerar que habrá horas de demanda alta dependiendo de la hora del día, exámenes próximos o momento del semestre. Por lo tanto, el sistema debe ser capaz de soportar por lo menos 200 usuarios al mismo tiempo. Estos usuarios podrán hacer cualquiera de las diferentes activades (iniciar sesión, pedir comida, hacer un entrega) en la aplicación sin que esta tenga problemas. 
### 5.2 Safety Requirements
Es necesario aplicar los mecanismos de seguridad necesarios para cuidar la integridad de los datos de los usuarios. La pérdida o filtración de información personal de los usuarios podría implicar problemas de seguridad, ya que como toda aquella persona registrada en esta plataforma es parte de la institución, tenemos que proteger sus datos para asegurarnos de que no se pueda utilizar de forma corrupta la información que nos proporcionaron. Asimismo, como se necesita introducir número de tarjeta para realizar los diferentes tipos de pagos, es esencial contar con un mecanismo de encripción que proteja los números de las tarjetas, su fecha de expiración y CVC. La pérdida de esta información implicaría problemas legales serios para EATAM. 
### 5.3 Security Requirements
Es necesario encontrar un método más seguro para verificar que la persona que se registra sí forma parte de la institución. Actualmente, la forma de verificar es que el registro se haga utilizando el correo institucional. 
### 5.4 Software Quality Attributes
  - **Portabilidad:** El sistema debería de funcionar para dispositivos tanto Android como iOS. Sin embargo, por el momento solo funciona para iOS, en específico dentro de un iPhone X. 
  - **Confiabilidad:** El sistema debe realizar las transacciones correctamente y tener la disponibilidad requerida para asegurar una confiabilidad de 98% 
  - **Mantenibilidad:** El sistema debe poder mejorse y corregirse de manera sencilla y clara. 
  - **Facilidad de testeo:** Las pruebas del producto son sencillas, sin embargo, el pago y cobro la única forma de probarlos completamente es haciendo un pedido real. 
  - **Reusabilidad:** El sistema puede adaptarse para utilizarse para cualquier otra institución que desee tener un servicio de pedido y entrega dentro de su comunidad. Lo único que debe ajustarse son las condiciones de registro y restricciones de entrega, así como el menú de productos ofrecidos. 
### 5.5 Business Rules
El uso de este sistema está limitado a la comunidad del Instituto Tecnológico Autónomo México, ya sea estudiante, catedrático o personal con otro cargo que trabaje dentro de la instituciones. Esto se debe a que el repartidor tendrá que entrar a las instalaciones para entregar la orden, por lo que es necesario que tenga permiso para ingresar. Asimismo, la recepción de órdenes se límita a los horarios en que los restaurantes estén abiertos. 

# Plan de calidad
## 1. Test Plan Identifier
JustInMind Prototyper 8.7.4
## 2. References
JustInMind Prototyper 8.7.4
https://www.youtube.com/watch?v=Y-JqVKQwdPE
https://www.youtube.com/watch?v=bdyDSOHe4ZY
Tecnologías Rappi, S.A.P.I. de C.V.
UBER B.V.
## 3. Introduction
De manera singular, el objetivo del proyecto es crear un prototipo que simule un sistema gig economy, utilizando como base el ITAM. Sin embargo, si nos vamos más allá de lo singular, el objetivo de este proyecto principalmente es identificar todos los elementos que pueden ser estandarizados, evaluados y gestionados en un proyecto, conocer la importancia de la documentación y el manejo de un proyecto y por suuesto se presenta la dificultad que abarca el trabajo en equipo.  
## 4. Test Items
- Validación correcta de que el usuario o contraseña sean correctos.
- Que el sistema no permita una petición de un restaurante o tienda que esté cerrado.
- Que las pantallas se desplieguen correctamente.
- Que los botones direccionen a las pantallas correctas.
- Que los botones tengan los links correctos.
## 5. Software Risk Issues
- Que el sistema bancario este fuera de servicio.
- Que el servidor de la aplicación se encuentre fuera de servicio.
- Que el pago del repartidor le llegue en tiempo y forma.
## 6. Features to be Tested
- Que los cálculos de los elementos agregados en el carrito sean correctos.
- Que el código de pago este bien generado.
- Que el sistema valide correctamente que la tarjeta de crédito o débito este registrada en un banco.
- Que el sistema valide correctamente el correo del usuario esté registrado en la base de datos del ITAM.
- Que el sistema calcule el promedio de las calificaciones de manera correcta.
- Que las gráficas muestres información verídica y confiable.
## 7. Features not to be Tested
- Que las preguntas frecuentes realmente sean frecuentes.
- Que el usuario tenga señal para llamar a atención a clientes.
- Que el usuario tenga wi-fi o datos móviles para utilizar la aplicación.
- Que el usuario no tenga bloqueos en sus tarjetas de crédito y/o débito.
## 8. Approach
Se ha considerado realizar este prototipo con JustInMind Prototyper, ya que este programa es el más adecuado para lo que se necesita. En este programa se ha decidido crear el prototipo con el iPhone X ya que en promedio es el tipo de celular más usado en el ITAM.
Se ha considerado que el prototipo del aplicativo únicamente podrá ser utilizado para sistema operativo iOS11 o superior.
Se estableció que el pago sería por tarjeta únicamente ya que el manejo de dinero físico podría ser alterado y sesgado debido a que se espera que los pedidos no abarquen montos tan altos.
El proyecto debe tener la posibilidad de registrar usuarios para que estos puedan ser identificados, ya sea para repartir o para recibir pedidos. Es por esto que el aplicativo debe tener una sección para cada enfoque, estas secciones deberán tener distintas configuraciones que coincidan con las tareas de los usuarios de cada sección. El repartidor tendrá que tener elementos estadísticos que le ayuden a conocer su rendimiento, ya sean calificaciones, así como ingresos semanales para conocer su desempeño. Mientras que el comensal debe de tener la oportunidad de calificar y recibir en su ubicación lo que desee de lugares que se encuentren cerca del ITAM.
El objetivo de esto es facilitar el acceso a los alimentos y bebidas cercanos al ITAM y al mismo tiempo ofrecer una posibilidad de obtención de ingresos mientras el usuario estudia.
Será importante considerar que el tiempo de entrega en algunas ocasiones podrá extenderse debido a que las ubicaciones pueden no ser 100% exactas, además, el conocimiento del campus para el repartidor será esencial, por lo que tendrá que aprender en la práctica de su labor en caso de que no lo conozca correctamente. 
## 9. Item Pass/Fail Criteria
Respecto al criterio de fallas, se espera que a niveles de interfaz: íconos, pantallas, links, etc., todos los elementos puedan ser probados y comprobar que funcionan correctamente.
Sin embargo, a un nivel más alto, ya de infrasestructura, se espera que todos los elementos puedan ser probados, pero que un porcentaje pequeño de ellos tenga algunas fallas insignificantes, por ejemplo, falla en la validación de "ñ" o acentos en los nombres, etc.
## 10. Suspension Criteria and Resumption Requirements
- Se deberá dejar de realizar pruebas cuando las primeras dos veces el sistema identifique una tarjeta no existente y una sí existente, es decir, una vez que se compruebe que la validación fue exitosa.
- También se dejarán de hacer pruebas sobre delays en el sistema, que tarde un poco más de lo acotumbrado en desplegarse una pantalla o en realizarse una instrucción.
- No continuar con pruebas de un mejor diseño de los elementos de la aplicación.
## 11. Test Deliverables
- Documentación general de las pruebas de EATAM.
- Documentación específica de las pruebas de EATAM (análisis de los elementos de cada sección: Comensal y Repartidor).
- Capturas de pantalla para comprobar que funciona correctamente o comprobar que no funciona correctamente cierta funcionalidad.
- Registros de error en cada sección.
- Análisis avanzado del margen de error del proyecto.
## 12. Remaining Test Tasks

## 13. Environmental Needs
## 14. Staffing and Training Needs
## 15. Responsibilities
## 16. Schedule
## 17. Planning Risks and Contingencies
## 18. Approvals
## 19. Glossary

# Arquitectura
EATAM maneja varias arquitecturas, la principal es por eventos ya que el sistema debe identificar cuando un evento (pedido) es asignado a un repartidor para que otro evento no sea asignado a ese mismo repartidor en ese momento. Además, debe distinguir entre un pedido y otro. Administra los pedidos de acuerdo al orden en el que fueron hechos y se asignan de manera que no haya repetidos o empalmen. También maneja microservicios, ya que utilizará los usuarios registrados en la base de datos del ITAM, así como la de las tarjetas de los bancos para identificar si sí están registradas en alguno de estos.

# Metodología
La metodología que utilizamos para realizar este proyecto fue Feature Driven. Partiendo de un bosquejo muy básico de lo que la aplicación debía realizar, en primer lugar, dividimos las funcionalidades en 3 según el modo al que pertenecen: comensal, repartidor y en general. Cada una de estas funcionalidades principales consiste en la agrupación de otras funcionalidades que hacen que el sistema funcione, las cuales fueron detalladas en segundo lugar mediante issues. Posteriormente, se realizó el seguimiento del desarrollo de cada modo mediante proyectos en GitHub cuyas tareas eran dichos issues. Elegimos esta metodología porque consideramos que por el tipo de problema era la mejor opción, ya que debíamos concentrarnos en que la aplicación pudiera hacer procesos específicos caracterizados por el tipo de usuario.

# Documentación para replicar
