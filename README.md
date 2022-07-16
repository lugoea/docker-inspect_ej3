## Instrucciones 

*   Ejecutar los siguientes comandos para obtener las imagenes a obtener:

```plaintext
docker pull  nicopaez/passwordapi-java:java8-alpine
docker pull nicopaez/passwordapi-java:java8-fabric
```

*   Utilizar el docker inspect nicopaez/passwordapi-java:java8-alpine y docker inspect nicopaez/passwordapi-java:java8-fabric Para obtener el detalle de layers de ambas imagenes.
*   Copiar la sección de layers con sus respectivos hash para ver si hay alguno similar.
*   Se debe tomar en consideración la sección del JSON de Layers, en donde se verifica que el hash  "sha256:73046094a9b835e443af1a9d736fcfc11a994107500e474d0abf399499ed280c" es comun entre ambas imagenes 
*   Tambien se puede descargar la herramienta dive Para Windows desde la url

 [https://github.com/wagoodman/dive/releases/download/v0.9.2/dive_0.9.2_windows_amd64.zip](https://github.com/wagoodman/dive/releases/download/v0.9.2/dive_0.9.2_windows_amd64.zip)

*   Y con hacer la misma validación para las dos imagenes descargadas anteriormente, comparando los sha256 de cauda layer. 
*   Otro comando interesante para considerar a efectos de intender que representa cada una de estas capas es docker history. Un ejemplo de uso seria

```plaintext
docker history --no-trunc  nicopaez/passwordapi-java:java8-alpine   
```