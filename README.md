# Modelo de ruteo para transporte de cacao en Arauca, Colombia
En el presente repositorio se encuentran los resultados principales y el código fuente relacionado con un modelo de ruteo implementado por etapas. El objetivo del ruteo es generar un transporte eficiente de mazorcas de cacao desde 180 fincas cacaoteras hacia 2 centrales post cosecha.
## Ubicación de Fincas y Centrales en el espacio

![](ImDOC/UbFyC.png)

Se cuentan con las coordenadas reales de la central 1, pero se tienen coordenadas teóricas para la central 2. Las 180 fincas se ven representadas como los puntos grises.

## Metodología empleada
La metodología desarrollada consta de 3 etapas. Primero, una etapa de asignación de cada finca a una de las dos centrales post cosecha. Segundo, una etapa de clustering que recibe por parámetro el número *k* de clusters que se deseen generar, etapa en la cual se evaluaron tres algoritmos diferentes. Y tercero, una etapa de ruteo con un modelo clásico de programación lineal que recibe por parámetro la capacidad *Q* de la flota de vehículos que se desea estudiar.

A continuación se encuentran enlaces que dirigen al código fuente desarrollado en cada una de las etapas junto con los resultados obtenidos:
- [Etapa 1 (Modelo de asignación lineal)](Scripts/Etapa1/Etapa1_Asignacion.ipynb)
- [Etapa 2 (Métodos de Clustering)](Scripts/Etapa2)
- [Etapa 3 (Modelo de ruteo)](Scripts/Etapa3/Etapa3_RuteoCVRP.ipynb)

## Modelo completo
Una vez fueron evaluadas cada una de las etapas por separado, se integraron en un mismo modelo que recibe por parámetros las coordenadas y la producción de las fincas, el número de clusters *k* y la capacidad de los camiones *Q*. 
Los resultados para valores de *k={5, 10, 15, 20}* y *Q={16, 28, 40, 52}* se ven en los siguientes enlaces (uno por cada central post cosecha): [Central 1](Scripts/ModeloCompleto/ModeloCompletoC1.ipynb), [Central 2](Scripts/ModeloCompleto/ModeloCompletoC2.ipynb).
