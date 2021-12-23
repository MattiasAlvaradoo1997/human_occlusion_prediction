# human_occlusion_prediction in PYTHON 3.8.8

predicción de movimiento de extremidades fuera del campo visual de la cámara



Primero asegúrate de instalar los requerimientos a partir de "requirements.txt" en un entorno virtual de python 3.8.8

Para utilizar el código, abre el archivo "patrak_human_occlusion.ipynb" y ejecuta todas las celdas. La sexta celda:

cap = cv2.VideoCapture("Untitled.mp4")
conf = 0.82
confizq= 0.78
confdist = 0.95
wind1 = 'Body occlusion'
wind2 = 'Skeleton'

...
...

ejecuta el modelo de predicción desde un video de entrenamiento físico. Para utilizar la cámara web se debe modificar la variable "cap" por:

cap = cv2.VideoCapture(0)


Se puede configurar el parámetro de confianza de visibilidad (para detectar oclusión) con la variable "conf" (82% de confianza para considerarse no ocluido);
la confianza de la visibilidad para la última distancia registrada (para determinar cuándo tomar la distancia de una extremidad no ocluida) con "confdist"
(95% de confianza para considerar la distancia entre puntos); y el tamaño del borde de la imagen con el parámetro "border".

Además, se puede obtiene la variable "body_positions" (nombrada en la segunda celda) que describe la posición de todas las extremidades en la imagen, seguido 
de si está oculta (True) o descubierta (False)
