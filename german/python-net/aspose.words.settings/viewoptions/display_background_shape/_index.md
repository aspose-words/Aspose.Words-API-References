---
title: ViewOptions.display_background_shape property
linktitle: display_background_shape property
articleTitle: display_background_shape property
second_title: Aspose.Words for Python
description: "ViewOptions.display_background_shape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /de/python-net/aspose.words.settings/viewoptions/display_background_shape/
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
# Verwenden Sie einen HTML-String, um ein neues Dokument mit einer einfarbigen Hintergrundfarbe zu erstellen.
html = "<html>\n                <body style='background-color: blue'>\n                    <p>Hello world!</p>\n                </body>\n            </html>"
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.unicode())))
# Die Quelle für das Dokument hat einen einfarbigen Hintergrund,
# dessen Vorhandensein wird das Flag "DisplayBackgroundShape" auf "true" setzen.
self.assertTrue(doc.view_options.display_background_shape)
# Behalten Sie "DisplayBackgroundShape" auf "true", um das Dokument die Hintergrundfarbe anzeigen zu lassen.
# Dies kann einige Textfarben beeinflussen, um die Sichtbarkeit zu verbessern.
# Setzen Sie "DisplayBackgroundShape" auf "false", um die Hintergrundfarbe nicht anzuzeigen.
doc.view_options.display_background_shape = display_background_shape
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayBackgroundShape.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

