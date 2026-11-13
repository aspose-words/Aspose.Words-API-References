---
title: ViewOptions.display_background_shape property
linktitle: display_background_shape property
articleTitle: display_background_shape property
second_title: Aspose.Words for Python
description: "ViewOptions.display_background_shape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /es/python-net/aspose.words.settings/viewoptions/display_background_shape/
---

## ViewOptions.display_background_shape property

Controls display of the background shape in print layout view.


```python
@property
def display_background_shape(self) -> bool:
    ...

@display_background_shape.setter
def display_background_shape(self, value: bool):
    ...

```

### Examples

Shows how to hide/display document background images in view options.

```python
# Utilice una cadena HTML para crear un nuevo documento con un color de fondo plano.
html = "<html>\n                <body style='background-color: blue'>\n                    <p>Hello world!</p>\n                </body>\n            </html>"
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.unicode())))
# La fuente del documento tiene un fondo de color plano,
#  cuya presencia establecerá la bandera "DisplayBackgroundShape" a "true".
self.assertTrue(doc.view_options.display_background_shape)
# Mantenga "DisplayBackgroundShape" como "true" para que el documento muestre el color de fondo.
# Esto puede afectar algunos colores de texto para mejorar la visibilidad.
# Establezca "DisplayBackgroundShape" a "false" para no mostrar el color de fondo.
doc.view_options.display_background_shape = display_background_shape
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayBackgroundShape.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

