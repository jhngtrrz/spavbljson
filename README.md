# Proyecto Conversión Biblia a JSON

## Descripción

Este proyecto toma la versión de la Biblia libre en formato texto plano (`spavbl_vpl.txt`) y la convierte a un formato JSON organizado para facilitar su uso en aplicaciones y análisis.

## Versión

**Versión actual: 1.0.8**

- **MAJOR**: Cambios incompatibles (ej. reestructuración completa del JSON).
- **MINOR**: Nuevas funcionalidades compatibles (ej. agregar metadatos o herramientas adicionales).
- **PATCH**: Correcciones de errores o mejoras menores.

## Fuente de Datos

El archivo de entrada `spavbl_vpl.txt` contiene el texto completo de la Biblia en el siguiente formato:

```
GEN 1:1 En el principio, Dios creó los cielos y la tierra.
GEN 1:2 La tierra carecía de forma y estaba vacía; la oscuridad cubría la superficie del abismo y el Espíritu de Dios se movía sobre la superficie de las aguas.
GEN 1:3 Y Dios dijo: “¡Que haya luz!” y hubo luz.
...
```

Este archivo es proporcionado por [eBible.org](https://ebible.org/details.php?id=spavbl) y está diseñado para ser importado en programas de estudio bíblico como BibleWorks. Contiene únicamente el texto bíblico sin formato adicional, notas o secciones no canónicas.

## Estructura del JSON de Salida

El archivo de salida `spavbl.json` tendrá una estructura organizada jerárquica basada en la conversión del texto plano:

```json
{
  "biblia": {
    "vbl": {
      "nombreCompleto": "Versión Bíblia Libre",
      "at": {
        "gen": {
          "nombre": "Génesis",
          "categoria": "Pentateuco",
          "capitulo": {
            "1": {
              "1": "En el principio, Dios creó los cielos y la tierra.",
              "2": "La tierra carecía de forma y estaba vacía; la oscuridad cubría la superficie del abismo y el Espíritu de Dios se movía sobre la superficie de las aguas.",
              "3": "Y Dios dijo: \"¡Que haya luz!\" y hubo luz.",
              ...
            },
            "2": {
              "1": "La creación de los cielos, la tierra y todo lo que hay en ellos quedó terminada.",
              ...
            }
          }
        },
        "exo": {
          "nombre": "Éxodo",
          "categoria": "Pentateuco",
          "capitulo": {
            ...
          }
        },
        ...
      }
    }
  }
}
```

Esta estructura refleja la organización del archivo JSON existente, con libros en minúsculas (ej. "gen", "exo"), incluyendo nombre y categoría para cada libro, y capítulos con versículos numerados.

## Contribución

Si deseas contribuir, por favor sigue las mejores prácticas para el manejo de textos sagrados.

## Licencia

El texto de la Biblia utilizado en este proyecto es la **Versión Biblia Libre** (Free Bible Version), copyright © 2018-2020 Jonathan Gallagher y Shelly Barrios de Avila. Está disponible bajo la licencia **Creative Commons Attribution Share-Alike 4.0 (CC BY-SA 4.0)**.

Esta licencia es permisiva y permite:

- Compartir y redistribuir el texto en cualquier formato.
- Hacer revisiones y adaptaciones razonables.

Con las siguientes condiciones:

- Debes incluir la información de copyright y fuente original.
- Si realizas cambios, debes indicar claramente que los hiciste y que el licenciante original no necesariamente respalda tus cambios.
- Si redistribuyes, debes hacerlo bajo la misma licencia (CC BY-SA 4.0).

Para más detalles, consulta los términos completos en [Creative Commons](https://creativecommons.org/licenses/by-sa/4.0/) o el sitio de eBible.org.

Nota: Revisar y adaptar la Palabra de Dios implica una gran responsabilidad para ser fiel a ella (ver Apocalipsis 22:18-19).

---

_Proyecto actualizado el 20 de septiembre de 2025._
