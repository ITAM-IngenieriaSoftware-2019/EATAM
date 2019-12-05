# EATAM
Projecto final equipo Los Tecolotes (la comida)

Integrantes:
- Amanda Velasco Gallardo             154415
- Tábata Ailé González Alvarado       155999
- Víctor Hugo Flores Pineda           155990
- Juan José

# System Requirements
## 1.Introduction 
### 1.1 Purpose 
EATAM es un sistema de gig economy para los alumnos, profesores y personal que forman parte del Instituto Tecnológico Autónomo de México. En este sistema podrán pedir o entregar comida a quien lo solicite dentro de las instalaciones de la institución. La finalidad de este producto es que los usuarios puedan pedir comida y/o ganar dinero extra en su tiempo libre. 
### 1.2 Document Conventions
### 1.3 Intended Audience and Reading Suggestions
El documento está planeado para ser leído por desarrolladoras, esto con la intención de poder ser mejorado y actualizado en el futuro. Por lo tanto, en el documento se expondrán los detalles técnicos necesarios del sistema. Se recomienda que la lectura de este sea en orden cronólogico. Además, se podrán encontrar referencias para el conocimiento y desarrollo de partes específicas del sistema. 
### 1.4 Product Scope 
El objetivo de este sistema se divide en dos. El primero es el de facilitar al usuario comensal la acción de ir por alimentos hasta su establecimiento deseado. El segundo objetivo es para el usuario repartidor y es poder recibir un ingreso en su tiempo libre en la institución. 
### 1.5 References
El sistema se creó utilizando [Just in mind prototyper](https://www.justinmind.com/), que es una plataforma para realizar propototipos de aplicaciones para diferentes positivos. 
Los íconos que se utilizaron para la elaboración de la aplicación se obtuvieron de: 
  - [FontAwesome](https://fontawesome.com/)
  - [Flaticon](https://www.flaticon.com/home)

## 2. Overall Description 
### 2.1 Product perspective
Esta versión es la primera del sistema y este surge tras analizar la necesidades de la comunidad. Muchas veces, por estar trabajando en cosas personales o de la institución, la comunidad prefiere continuar con sus deberes que comer. Además, este sistema crea una oportunidad de trabajo flexible. Por lo tanto, se busca satisfacer dos necesidades de la comunidad y que sea la comunidad la que las satisfaga. 
### 2.2 Product Functions 
Como ya se ha hecho hincapié anteriormente, el sistema se puede dividir en dos entidades. Por lo mismo, las funciones del sistema se dividen en dos. 

Funciones para el comensal: 
 - comprar: 

Funciones para el repartidor: 
  - Modo repartidor: el usuario podrá definir si desea estar activo como repartidor. En caso de estar activo cuando se haga una petición de orden podrá recibirla y hacer lo necesario para que el comensal reciba su pedido. 
  - Recoger y entregar la orden: el usuario podrá aceptar o rechazar una orden. Si el usuario la acepta, se despliega la información sobre la orden, por ejemplo, dónde tiene que recogerla, los productos que tiene que recoger, a dónde la tiene que llevar y la información sobre el comensal que hizo la orden. 
### 2.3 User Classes and Characteristics
### 2.4 Operating Environment 
Por restricciones definidas por **Just in mind**, que es que se trabaja sobre la pantalla de un dispositivo en específico y para replicar a otros hay que ajustarlo manualmente, el sistema está hecho para trabajar solamente en la pantalla de un iPhone X. Por lo mismo, las llamadas a los usuarios solo corresponden a las pantallas establecidas por el sistema operativo iOS y excluyen a las de Android. 
### 2.5 Design and Implementation Constraints
Durante el semestre y horas del día, el sistema tendrá una demanda distinta, por ejemplo, en finales y antes de los exámenes de economía habrá más demanda de comensales debido a que muchos estudiantes preferirán que la comida se les lleve al lugar de estudio en vez de ellos salir por ella. Además, se debe tomar en consideración las áreas en que está prohibido introducir comida, por ejemplo, la biblioteca. Asimismo, considerar que es necesario especificar las restricciones para la entrega de comida, con tal de no interrumpir una clase para hacer la entrega. 
### 2.6 User Documentation 
### 2.7 Assumptions and Dependencies

## 3. External Interface Requirements
### 3.1 User Interfaces
### 3.2 Hardware Interfaces
### 3.3 Software Interfaces
### 3.4 Communication Interfaces

## 4. System Features

**Features comunes a todos los usuarios**
### 4.1 [Entrada al sistema con credenciales de usuario](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/1)
### 4.2 [Registro de nuevo usuario](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/5)
### 4.3 [Configuraciones de la cuenta del usuario](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/9)

**Features del modo Comensal**

**Features del modo Repartidor**
### 4. [Menú para navegar por las funcionalidades del Repartidor](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/6)
### 4. [Perfil del usuario y activación del modo Repartidor](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/13)
### 4. [Información del pedido en curso que el usuario Repartidor está completando](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/8)
### 4. [Modificación de métodos en que el usuario Repartidor recibe sus pagos](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/12)
### 4. [FAQs y contacto a soporte para el usuario Repartidor](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/11)
### 4. [Notificaciones de pedidos entrantes](https://github.com/ITAM-IngenieriaSoftware-2019/EATAM/issues/7)

## 5. Other Nonfunctional Requirements
### 5.1 Performance Requirements
Es necesario considerar que habrá horas de demanda alta dependiendo la hora del día, exámenes próximo o momento del semestre. Por lo tanto, el sistema debe ser capaz de soportar por lo menos 200 usuarios al mismo tiempo. Estos usuario podrán hacer cualquiera de las diferentes activades (iniciar sesión, pedir comida, hacer un entrega) en la aplicación sin que esta tenga problemas. 
### 5.2 Safety Requirements
Es necesario aplicar los mecanismos de seguridad necesarios para cuidar la integridad de los datos de los usuarios. La pérdida o filtración de infromación personal de los usuarios podría implicar problemas de seguridad, ya que como toda aquella persona registrada en esta plataforma es parte de la institución tenemos que proteger sus correos para asegurarnos de que no se puede utilizar de forma corrupta la información que nos proporcionaron. Asimismo, como se necesita introducir número de tarjeta para realizar los diferentes pagos es esencial contar con mécanismo que protejan los números de las tarjetas, fecha y CVC. La pérdida de sta información implicaría problemas legales serios para EATAM. 
### 5.3 Security Requirements
Es necesario encontrar un método más seguro para verificar que la persona que se registra si forma parte de la institución. Actualmente, la forma de verificar es que el registro se haga utilizando el correo de la institución. 
### 5.4 Software Quality Attributes
  - **Portabilidad:** El sistema debería de funcionar para dispositivos tanto Android como IOS. Sin embargo, actualmente solo funciona para IOS. 
  - **Confiabilidad:** El sistema debe realizar las transacciones correctamente y tener la disponibilidad requerida paraasegurar una confiabilidad de 98% 
  - **Mantenibilidad:** El sistema debe poder mejorse y corregirse de manera sencilla y clara. 
  - **Facilidad de testeo:** Las pruebas del producto son sencillas, sin embargo, el pago y cobro la única forma de probarlos es haciendo un pedido real. 
  - **Reusabilidad:** El sistema puede adaptarse para utilizarse para cualquier otra institución que desee tener un servicio de pedido y entrega de como dentro de su comunidad. Lo único que debe ajustarse son las condiciones de registro. 
### 5.5 Business Rules
El uso de este sistema está limitado a la comunidad del Instituto Tecnológico Autónomo México, ya sea estudiante, catedrático o personal con otro cargo que trabaje dentro de la instituciones. Esto se debe a que el repartidor tendrá que entrar a las instalaciones para entregar la orden, por lo que es necesario que tenga permiso para ingresar. Asimismo, la recepción de órdenes se límita a los horarios en que los restaurantes estén abiertos. 

# Plan de calidad

# Arquitectura

# Metodología
