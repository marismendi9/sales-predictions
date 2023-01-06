# Predicción de ventas alimenticias cadena de tiendas



**Objetivo del proyecto:**
- Saber qué tan bien se pueden predecir las ventas de productos de una cadena de tiendas.

**Conjunto de datos:**
| Nombre de la variable     | Descripción                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Item_Identifier           | Identificación única del producto                                                                                     |
| Item_Weight               | Peso del producto                                                                                                     |
| Item_Fat_Content          | Si el producto es bajo en grasa o regular                                                                             |
| Item_Visibility           | El porcentaje de la superficie total de exposición de todos los productos de una tienda asignada al producto concreto |
| Item_Type                 | La categoría a la que el producto pertenece                                                                           |
| Item_MRP                  | Precio máximo de venta al público (precio de catálogo) del producto                                                   |
| Outlet_Identifier         | Identificación única de la tienda                                                                                     |
| Outlet_Establishment_Year | El año cuando se estableció la tienda                                                                                 |
| Outlet_Size               | El tamaño de la tienda con respecto a la superficie                                                                   |
| Outlet_Location_Type      | El tipo de área donde está ubicada la tienda                                                                          |
| Outlet_Type               | Si el marcado es un almacén o algún tipo de supermercado                                                              |
| Item_Outlet_Sales         | Ventas del producto en la tienda particular Es la variable objetivo a predecir                                        |  

**Visualizaciones obtenidas del dataset:**

![image](https://user-images.githubusercontent.com/112273414/208545659-39117277-47ee-4326-b8dd-71da0ee7c0d6.png)

![image](https://user-images.githubusercontent.com/112273414/208545689-9416fe18-1316-43a9-b00d-1ad41a720d3f.png)

![image](https://user-images.githubusercontent.com/112273414/208545707-d0270f5f-0336-4f4b-9e13-400794ae9698.png)

**Observaciones del análisis exploratorio:**

Los datos presentan una alta variabilidad respecto a unas tiendas y a otras; volumen de ventas independiente en la mayoría de los casos del tamaño de la tienda así como tiendas que venden más cierto tipos de productos que otras.

Se aplican los modelos de regresión lineal y de árbole de regresión (con la misma semilla para ambos) y se comparan los resultados.

**Resumen de los resultados:**

El modelo que 'mejor resultado' arrojó ha de ser el de árbol de regresión; sin embargo, su R2 continúa siendo muy bajo y a pesar de que se pudo reducir su varianza, su error continúa siendo muy alto.

Yo recomendaría no aplicar un modelo de esta forma, hacer más análisis como investigar qué variables no infieren tanto en el vector objetivo, así como segmentar las predicciones para cada outlet, ya que por las características tan variadas de estas, podríamos sesgar la muestra que es lo que vemos con el R2 actual, que parece estar subajustado por la aleatoriedad de los datos mismos.

Así que en ese orden de ideas, aún no recomendaría ningún modelo: analizaría las variables más importantes y eliminaría aquellas que no pesen tanto en la predicción (baja interdependencia), dividiría el dataframe por outlet y por tipo de producto para realizar las predicciones, luego probaría este y otros modelos que me den resultados óptimos.

Finalmente con los resultados obtenidos podría tomaría decisiones de negocio objetivas y más acertadas.
