---
title: ViewOptions.display_background_shape property
linktitle: display_background_shape property
articleTitle: display_background_shape property
second_title: Aspose.Words for Python
description: "ViewOptions.display_background_shape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /fr/python-net/aspose.words.settings/viewoptions/display_background_shape/
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
# Utilisez une chaîne HTML pour créer un nouveau document avec une couleur d'arrière-plan unie.
html = "<html>\n                <body style='background-color: blue'>\n                    <p>Hello world!</p>\n                </body>\n            </html>"
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.unicode())))
# La source du document possède un arrière-plan de couleur unie,
# dont la présence définira le drapeau "DisplayBackgroundShape" sur "true".
self.assertTrue(doc.view_options.display_background_shape)
# Conservez "DisplayBackgroundShape" à "true" pour que le document affiche la couleur d'arrière-plan.
# Cela peut affecter certaines couleurs de texte pour améliorer la visibilité.
# Définissez "DisplayBackgroundShape" sur "false" pour ne pas afficher la couleur d'arrière-plan.
doc.view_options.display_background_shape = display_background_shape
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayBackgroundShape.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

