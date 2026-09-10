1.1

Qué está mal? Tenemos duplicidad de codigo
Que archivo y que líneas se manifiesta? Existe steps en los jobs que son basicamente lo mismo como Descargar el Codigo o Instalar Dependencias
Qué consecuencia tiene? Genera mas demora a la hora de ejecutar el pipeline y mayor procesamiento computacional

Qué está mal? Tenemos una version de python que solo está en 3.11 no es especifica
Que archivo y que líneas se manifiesta? Se manifiesta en los steps de preparacion de Python y a la hora de instalar dependencias
Qué consecuencia tiene? Puede ocurrir que agarre una version de python que no sea compatible con alguna libreria por su version. Tiene una desventaje en la reproducibilidad

Qué está mal?   No existe un caché de dependencias
Que archivo y que líneas se manifiesta? A la hora de preparar Python
Qué consecuencia tiene? Hace que cada build demore, ya que no se tiene un cache. Con el cache hace que el pipeline corra mas rapido y no demore tanto 

Qué está mal?  Falta la dependencia explicita entre jobs
Que archivo y que líneas se manifiesta? A la hora de hacer el job de Publicar
Qué consecuencia tiene? No valida que se haya terminado el job anterior correctamente y aun asi puede ejecutar el siguiente job. Puede tener un gran problema a la hora de reproducibilidad y dañar el flujo

1.2
El que puede explicar mas esto es el de cache, ya que no se almacena un cache y por ello en la segunda o tercera vez que se ejecuta el pipeline demora casi lo mismo. 

1.3
Para el VSM se ve afectado con la demora del pipeline (tiempo de espera), es un punto clave ya que tenemos el tiempo del proceso que es lo que se demora una persona trabajando mientras que el tiempo de espera es lo 
que se demora el pipeline lo que aumenta el lead time

1.4
La métrica DORA que esperamos mover es la Lead Time para cambios ya que si reducimos los defectos identificados y tenemos un pipeline eficiente y correcto podremos reducir el lead time de despliegue y tener mayor eficiencia

1.5
Especialmente mediremos cuanto se demora el workflow en ejecutar pasaremos de 1m y 3 segundos a menos de 1 min
