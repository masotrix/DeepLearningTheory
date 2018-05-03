### 1. Very Large Conv, 2014 [https://arxiv.org/abs/1409.1556]

- Uso de pequeños campos receptores (3x3).
- Aumento de cantidad de capas convolucionales.

# Análisis

- En el pasado se utilizaron unos de tamaños 11x11 y 7x7.
  Los campos receptores disminuidos permiten de este modo
  la adición de una mayor cantidad de capas, y por lo
  tanto, una mayor cantidad de discriminación/abstracción
  a través de la no linealidad de las funciones de
  activación ReLu.
- Dos campos receptores 3x3 apilados (con stride 1) generan
  implícitamente un campo receptor 5x5, es decir, incorporan
  y concentran equivalente información adyacente, permitiendo 
  además que ésta tenga un significado más rico y abstracto.
- También se utiliza una menor cantidad de parámentros,
  lo que permitiría generar cierto tipo de regularización.
- Finalmente, utilizan una menor cantidad de conexiones,
  lo que disminuye la carga computacional y permite por lo
  tanto la adición de capas.
  
  ### 2. 
