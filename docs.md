Para correr en local

- en `compose.yml` el `cloud-config-container` esta apuntando a el zipkin pero como si estuviera corriendo en su propio host y no en la red interna, entonces se debe cambiar el nombre del contenedor de `zipkin-container` a `zipkin` y agregar la siguiente variable al entorno de `cloud-config-container`: `- SPRING_ZIPKIN_BASE-URL=http://zipkin:9411`