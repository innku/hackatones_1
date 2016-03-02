# hackatones

Este proyecto está pensado para ofrecer una opción no difícil de implementar y accesible para gestionar información relacionada a un hackatón.

La información está distribuida en bloques por lo que cada uno de ellos tiene un archivo independiente que puedes editar para incluir la tuya.

Este tema está pensado para usar dos escenarios: uno antes/durante y uno posterior o al cierre del evento.

El antes/durante, inicia desde que ya se ha decidido y logrado concretar los aspectos operativos de un hackatón. Aquí la información debe ser clara, puntual y se tiene que adelantar a responder a las preguntas más comunes que puedan tener los interesados.

El escenario posterior, comienza a ser útil una vez que el hackatón a llegado a su término, es ideal hacer saber de manera pública cuáles fueron los logros que se obtuvieron, así como quienes fueron los ganadores.

Hacer el cambio de escenario implica modificar algunos datos.

Cabe mencionar que la apariencia del contenido es responsivo y editable. Funciona utilizando plataformas como http://jekyllrb.com/ y servicios como https://github.com/, entre otros.

## Instalación
Para una instalación fácil, deberás tener presente ciertos requerimientos y comandos, para ello consulta `http://jekyllrb.com/docs/quickstart/`

Debes bajar el tema [desde aquí](https://github.com/), depués tendrás que mover la carpeta a su ubicación definitiva y desde la terminal entra al directorio y corre el comando `bundle exec jekyll serve`

Antes de subir tu sitio, realiza los cambios necesarios en `_config.yml`

1. Si estás almacenando tu sitio en GitHub tu `url` debería ser `http://nombre-de-usuario.github.io` si necesitas información al respecto consulta `https://pages.github.com/`

2. En `baseurl` se encuentra la sub-ruta para tu sitio. Si el repositorio se llama `hackatones`, este debería estar en `/hackatones`

3. En `tracking_id` puedes establecer tu identificador para google analytics. Para que funciones esta variable debe estár definida como `true`

## Uso

- Para hacer funcionar el servidor debes utilizar la línea `jekyll server --baseurl`

- La información para la página de inicio se puede modificar en `_data` y en `_config.yml`

  Para cambiar el texto al inicio del proyecto: `Título para el hackatón`, deberás cambiar `title:` en `_config.yml`

  Para cambiar la imagen de fondo que aparece en la página de inicio deberás reemplazar `img/background.jpg`por la que tu desees, las dimensiones de esta son: 1100 x 733 px

  En el caso de la sección Objetivo debes ir a `_data/goal.yml`
  Si deseas agregar fechas para la Agenda sólo debes seguir el formato en `_data/agenda/agenda.yml`

  Para el mapa, sólo necesitas cambiar el iframe que te proporciona google maps en `_data/map.yml` o incluir la estructura similar de otro servicio

  Para agregar jueces debes incluir las imágenes en `/img/judges` y cambiar la información tendrás que ir a `_data/judges/judges.yml`

  Los Premios manejan la misma lógica que Agenda, esta información se encuentra en `_data/awards/awards.yml`

  La sección de Resultados está pensada para incluir un texto que describa lo que se logró con el evento en términos cualitativos y cuantitativos, esto se debe cambiar en `_data/results.yml`

  Para Ganadores se usa la misma distribución que en Jueces, imágenes en `/img/winners` e información en `_data/winners/winners.yml`

- Para generar un nueva publicación en la sección de Noticias, sólo necesitas almacenar el archivo `.markdown` en el directorio `_posts/`

  Te recomendamos guardarlos con el siguiente formato `año-mes-día-Nombre-del-archivo.markdown`

  Las imágenes de los post deben estár en el directorio `/post-images` y el vínculo en el archivo almacenado en `_posts/` debe coincidir

- Para tener comentarios en los publicaciones, deberás utilizar Facebook comments.

  En caso de no querer utilizarlos se tiene que localizar en `_config.yml` el bloque `# Facebook comments` y cambiar a false la variable `fbcomments`.

  Para utilizarlos, es necesario tener validada la cuenta en Facebook (número telefónico) y estar registrado como desarrollador en `https://developers.facebook.com/`.

  Una vez que se tenga lo anterior, se tiene que crear una nueva aplicación en `My Apps`, selecionando como plataforma `Sitio web` para obtener tu número de identificación o `App Id`.

  El `App Id` y el `Api version`, deben ser reemplazados en `_config.yml`.

  Después, en `https://developers.facebook.com/docs/plugins/comments` debes agregar en `Comments Plugin Code Generator` el url que utilizarás para tu sitio, por último debes dar click en el botón `Get code`. Sólo necesitas generar el código desde la página para que la información que ya agregaste en `_config.yml` funcione.

- Este tema esta pensado para manejar una gama cromática específica, si deseas modificar los colores debes ir a `_sass/_site.scss` y ubicar el bloque `// Variables de color para el tema`

- Como se mencionó este tema está pensado para manejar 2 escenarios, uno previo/durante y otro posterior al evento. En `_config.yml`, encontrarás las `// Variables de contenido`, los valores definidos son para el escenario previo. Para el posterior, deberás invertir el valor de éstas variables.


## Licencia
MIT. Copyright (c) [Nombre del proveedor ](http://sitiodelproveedor.com)
