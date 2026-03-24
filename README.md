# PROYECTO DE ANÁLISIS DE DATOS SOBRE RENDIMIENTO LOGÍSTICO

### OBJETIVO
Una empresa de logística quiere entender qué factores influyen en la puntualidad de las entregas. El objetivo es analizar los patrones de envío para identificar áreas de mejora y proponer medidas estratégicas que mejoren la eficiencia del proceso logístico.

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

### DASHBOARD
[<img width="1619" height="1079" alt="Dashboard" src="https://github.com/user-attachments/assets/665c9108-6a46-44c7-88b0-959b01a5283a" />](https://public.tableau.com/views/Shipping_17743553116960/Dashboard?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### CONCLUSIONES
Tras el análisis de los datos de origen y la comprensión de los resultados obtenidos, se obtienen las siguientes conclusiones:
-	El 60% del total de los envíos sufrieron algún retraso.
-	El bloque de almacenamiento F concentra el doble de envíos que el resto. Sin embargo, el porcentaje de retrasos es muy similar en todos los bloques.
-	El barco es el modo de envío más frecuente con gran diferencia, aunque la tasa de retrasos permanece estable entre los diferentes métodos de envío.
-	Los productos de alta importancia son los que mayor porcentaje de retrasos presentan, a pesar de ser el tipo menos frecuente en el dataset.
-	Cuanto más caro es el producto, menor es el porcentaje de retrasos.
-	Los productos más pesados sufren menos retrasos.
-	Respecto al descuento aplicado, se diferencian dos comportamientos:
    - Con descuentos ≤ 10%, predominan los envíos a tiempo.
    - Con descuentos > 10%, todos los envíos presentan retrasos.
-	En cuanto a las variables relacionadas con la interacción del cliente:
    - Los clientes con menos compras previas sufren una mayor tasa de retrasos.
    -  Los retrasos provocan más llamadas al servicio de atención, disminuyendo por tanto el porcentaje de retrasos con el aumento del número de llamadas.
    - El retraso del producto no parece influir en la calificación del cliente. Otros factores pueden estar siendo más relevantes a la hora de calificar el producto.

### HALLAZGOS CLAVE Y PROPUESTAS
-	**Considerar mejorar el servicio a nuevos clientes**: los clientes con menos compras previas sufren retrasos en sus envíos más frecuentemente, lo que podría dificultar captar clientes habituales.
-	**Los productos más baratos y ligeros son los que más retrasos sufren**: revisar si se agrupan para ahorrar costes y eso condiciona que no lleguen a tiempo.
-	**Revisar las políticas de descuento**: ya que un descuento alto se asocia directamente con el retraso.
-	**Los productos de alta importancia son los que más retrasos sufren**: revisar la prioridad de sus envíos dada su categoría.
-	**Analizar la sobrecarga de almacenaje en el bloque F**: aunque no presente una mayor tasa de retrasos, una redistribución del inventario podría suponer una mejora general.
