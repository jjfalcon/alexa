# alexa

## 

[Alexa donde están mis llaves](https://twitter.com/vivirenremoto/status/1313772722539896834?s=12) con arduino+GPS, un servicio web y una app en Alexa puede ser la solucion...

[Cómo diseñar una (buena) Skill de Alexa](https://planetachatbot.com/como-disenar-skill-de-alexa-f5ef3cb2162c) Cualquier persona con conocimientos de desarrollo puede crear una Skill, pero hay que tener en cuenta diversos aspectos dentro del desarrollo de una Skill para poder crear una Skill de calidad, atractiva al usuario, que haga que el usuario quiera volver a usarla. Para ello la skill deben tener las siguietnes ciertas características:
* Internacionalizacion, en caso de usarse en distintas regiones, y debe ofrecer variedad en las respuestas.
* Persistencia de datos, es facil de implementar y marca la diferencia para adaptar respuestas al contexto del usuario. La primera vez hay que explicar bien la skill, pero luego no hace falta, etc.
* Atributos de sesion, permite almacenar datos recogidos durante la sesión para adaptar las respuestas. Un ejemplo podría ser una Skill donde preguntas el horario del colegio de uno de tus hijos, la primera vez te preguntará sobre que hijo quieres consultarlo, pero si haces mas preguntas siempre te responderá sobre ese hijo, que tendrá almacenado en memoria.
* Personalización de los mensajes, para dirigirnos al usuario por su nombre. A todos nos gusta!
* Permisos que se pueden conceder a la skill para mejorar su funcionamiento a la hora de ser lanzada (name, email, phone, reminders, location, etc)
* Integraciones con APIs externas, para aportar más información y mejorar la UX. Por ejemplo conectando con una API meteorológica que nos diga el tiempo del día que estamos preguntando en la localizacion.
* APL y/o APL-A, APL es una capa visual para reforzar mensaje, disponible en algunos dispositivos con pantalla. APL-A permite reproducir audio en el mismo instante que Alexa habla y da un toque de calidad a la Skill muy interesante.
* FallbackIntent es un intent donde llegarán todas aquellas peticiones que nuestra Skill no sepa manejar, lo que permite dar un mensaje menos “drástico o brusco” al usuario. Además nos permite recopilar la información que no hemos sabido capturar en otros intents.
* Interceptores, para unificar código que nos permita por ejemplo loggear el evento que nos llega para analizarlo posteriormente, limpiar las dynamic entities, etc..
* Entonación y diálogos, para que la comunicación parezca los mas humana posible. Con los tags de SSML podremos variar la velocidad con la que Alexa habla, hacer pausas, cambiar voces, etc. Lo que le dará a nuestra Skill un toque mucho más natural. Un ejemplo sería sí queremos que nuestra Skill diga un número de teléfono, por ejemplo 123 456 789, Alexa dirá ciento veintitrés millones…, y claro, muy natural no es. Sin embargo si usamos SSML con el tag interpret-as=”telephone”
```
<say-as interpret-as=”telephone”>123 456 789</say-as>
```
