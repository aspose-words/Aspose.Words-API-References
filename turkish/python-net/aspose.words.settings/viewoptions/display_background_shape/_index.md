---
title: ViewOptions.display_background_shape property
linktitle: display_background_shape property
articleTitle: display_background_shape property
second_title: Aspose.Words for Python
description: "ViewOptions.display_background_shape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /tr/python-net/aspose.words.settings/viewoptions/display_background_shape/
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
# Düz bir arka plan rengine sahip yeni bir belge oluşturmak için bir HTML dizesi kullanın.
html = "<html>\n                <body style='background-color: blue'>\n                    <p>Hello world!</p>\n                </body>\n            </html>"
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.unicode())))
# Belgenin kaynağı düz renkli bir arka plana sahiptir,
# bu varlık "DisplayBackgroundShape" bayrağını "true" olarak ayarlayacaktır.
self.assertTrue(doc.view_options.display_background_shape)
# "DisplayBackgroundShape" değerini "true" tutarak belgenin arka plan rengini göstermesini sağlayın.
# Bu, görünürlüğü artırmak için bazı metin renklerini etkileyebilir.
# "DisplayBackgroundShape" özelliğini "false" olarak ayarlayarak arka plan rengini göstermeyin.
doc.view_options.display_background_shape = display_background_shape
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayBackgroundShape.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

