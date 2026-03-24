# PROYECTO

### OBJETIVO
Una empresa de logística quiere entender qué factores influyen en la puntualidad de entregas. El objetivo es analizar los patrones de entrega para identificar áreas de mejora y proponer medidas estratégicas que mejoren la eficiencia del proceso logístico.

### BASE DE DATOS UTILIZADA
El dataset proviene de Kaggle y contiene 10.999 registros con la siguiente información acerca del envío:
- **ID**: Identificador del cliente o pedido.
- **Bloque del almacén**: A, B, C, D o F.
- **Método de envío**: avión, barco o carretera.
- **Número de llamadas de atención al cliente.**
- **Calificación del cliente**: 1 (peor) a 5 (mejor).
- **Precio del producto.**
- **Número de compras previas del cliente.**
- **Nivel de importancia del producto**: baja, media o alta.
- **Género del cliente.**
- **Descuento aplicado al producto.**
- **Peso del producto en gramos.**
- **Retraso**: variable (0 = a tiempo, 1 = retraso)

### METODOLOGÍA
1.	Se selecciona la base de datos y se realiza un análisis exploratorio mediante SQL para obtener los primeros insights.
2.	Se crean nuevas variables categorizadas, como grupos de productos por coste y por peso, con el fin de facilitar el análisis posterior.
3.	Se utiliza Tableau para construir un dashboard interactivo que permite visualizar los factores asociados a los retrasos.

### CONCLUSIONES
Tras el análisis de los datos de origen y la comprensión de los resultados obtenidos, se obtienen las siguientes conclusiones:
-	De los 10.999 envíos, 4.436 llegaron a tiempo mientras que 6.563 sufrieron algún tipo de retraso, lo que supone casi el 60% del total.
-	El bloque de almacenamiento F concentra el doble de envíos que el resto. Sin embargo, el porcentaje de retrasos es muy similar en todos los bloques.
-	El barco es el modo de envío más frecuente con gran diferencia, aunque la tasa de retrasos permanece estable entre los diferentes métodos de envío.
-	Los productos de alta importancia son los que mayor porcentaje de retrasos presentan, a pesar de ser el tipo menos frecuente en el dataset.
-	Al agrupar los productos en cuatro rangos de precio, se observa un patrón claro: cuanto más caro es el producto, menor es el porcentaje de retrasos.
-	De manera análoga, al clasificar los productos por grupos de peso, se observa que los productos más pesados sufren menos retrasos.
-	Respecto al descuento aplicado, se diferencian dos comportamientos:
	Con descuentos ≤ 10%, predominan los envíos a tiempo.
	Con descuentos > 10%, todos los envíos presentan retraso.
-	En cuanto a las variables relacionadas con la interacción del cliente:
	La calificación del cliente no parece influir en la tasa de retrasos.
	Los clientes con menos compras previas muestran una mayor proporción de 	retrasos.
	A medida que aumenta el número de llamadas al servicio de atención, 	disminuye el porcentaje de retrasos, lo que sugiere una posible relación entre 	la gestión del seguimiento y la puntualidad.

### HALLAZGOS CLAVE Y PROPUESTAS
-	Revisar las políticas de descuento: ya que un descuento alto se asocia con el retraso, interesaría analizar su posible relación con liquidación.
-	Los productos de alta importancia son los que más retrasos sufren: revisar la prioridad de sus envíos dada su categoría.
-	Analizar la sobrecarga de almacenaje en el bloque F: aunque éste no presente mayor tasa de retrasos, una redistribución del inventario podría suponer una mejora general.
-	Los productos más baratos y ligeros son los que más retrasos sufren: revisar si se agrupan para ahorrar costes y eso condiciona que no lleguen a tiempo.
