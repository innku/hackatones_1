# hackatones

## Instalación
Para una instalación fácil, deberás tener presente ciertos requerimientos y comandos, para ello consulta `http://jekyllrb.com/docs/quickstart/`

Antes de subir tu sitio, realiza los cambios necesarios en `_config.yml`

1. Si estás almacenando tu sitio en GitHub tu `url` debería ser `http://nombre-de-usuario.github.io`

2. En `baseurl` se encuentra la subruta para tu sitio. Si el repositorio se llama `hackatones`, este debería estar en `/hackatones`

3. En `tracking_id` puedes establecer tu identificador para google analytics. Para que funciones esta variable debe estár definida como `true`

## Uso

- Para hacer funcionar el servidor debes utilizar la línea `jekyll server --baseurl`

- La información para la página del inicio se puede modificar en `_data` y en `_config.yml`
  Para cambiar el `Título para el hackatón` deberás cambiar `title:` en `_config.yml`
  En el caso del Objetivo debes ir a `_data/goal.yml`
  Si desear agregar fechas para la Agenda sólo debes seguir el formato en `_data/agenda/agenda.yml`
  Para el mapa, sólo debes cambiar el iframe que te proporciona google maps en `_data/map.yml`
  Para agregar jueces debes incluir las imágenes en `/img/judges` y cambiar la información deberás ir a `_data/judges/judges.yml`
  Los Premios manejan la misma lógica que Agenda, este se encuentra en `_data/awards/awards.yml`
  La sección de Resultados está pensada para incluir un texto que describa lo que se logró con el evento, esto se debe cambiar en `_data/results.yml`
  Para Ganadores se usa la misma distribución que en Jueces, imágenes en `/img/winners` e información en `_data/winners/winners.yml`

  Esta tema está pensado para manejar 2 escenarios, uno previo y uno posterior. En `_config.yml`, encontrarás las Variables de contenido, los valores definidos son para el escenario previo. Para el posterior, deberás invertir el valor de éstas variables.

- Para generar un nuevo post, sólo necesitas almacenar el archivo `.markdown` en el directorio `_posts`

- Te recomendamos guardarlos con el siguiente formato `año-mes-día-Nombre-del-archivo.markdown`

- La imágenes de los post debe estár en el directorio `/post-images`

## Licencia
MIT. Copyright (c) [Nombre del proveedor ](http://sitiodelproveedor.com)
