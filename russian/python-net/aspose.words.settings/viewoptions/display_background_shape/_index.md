---
title: ViewOptions.display_background_shape property
linktitle: display_background_shape property
articleTitle: display_background_shape property
second_title: Aspose.Words for Python
description: "ViewOptions.display_background_shape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /ru/python-net/aspose.words.settings/viewoptions/display_background_shape/
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
# Используйте строку HTML для создания нового документа с однотонным фоном.
html = "<html>\n                <body style='background-color: blue'>\n                    <p>Hello world!</p>\n                </body>\n            </html>"
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.unicode())))
# Источник документа имеет однотонный цвет фона,
# наличие которого установит флаг "DisplayBackgroundShape" в значение "true".
self.assertTrue(doc.view_options.display_background_shape)
# Оставьте "DisplayBackgroundShape" в значении "true", чтобы документ отображал цвет фона.
# Это может изменить некоторые цвета текста для улучшения видимости.
# Установите "DisplayBackgroundShape" в значение "false", чтобы не отображать цвет фона.
doc.view_options.display_background_shape = display_background_shape
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayBackgroundShape.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

