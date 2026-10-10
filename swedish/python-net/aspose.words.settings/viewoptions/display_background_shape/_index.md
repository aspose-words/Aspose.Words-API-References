---
title: ViewOptions.display_background_shape property
linktitle: display_background_shape property
articleTitle: display_background_shape property
second_title: Aspose.Words for Python
description: "ViewOptions.display_background_shape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /sv/python-net/aspose.words.settings/viewoptions/display_background_shape/
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
# Använd en HTML-sträng för att skapa ett nytt dokument med en enfärgad bakgrund.
html = "<html>\n                <body style='background-color: blue'>\n                    <p>Hello world!</p>\n                </body>\n            </html>"
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.unicode())))
# Källan för dokumentet har en enfärgad bakgrund,
# vars närvaro kommer att sätta flaggan "DisplayBackgroundShape" till "true".
self.assertTrue(doc.view_options.display_background_shape)
# Behåll "DisplayBackgroundShape" som "true" för att få dokumentet att visa bakgrundsfärgen.
# Detta kan påverka vissa textfärger för att förbättra synligheten.
# Ställ in "DisplayBackgroundShape" till "false" för att inte visa bakgrundsfärgen.
doc.view_options.display_background_shape = display_background_shape
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayBackgroundShape.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

