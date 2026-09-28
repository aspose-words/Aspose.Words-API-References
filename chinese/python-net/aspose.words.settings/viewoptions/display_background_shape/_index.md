---
title: ViewOptions.display_background_shape property
linktitle: display_background_shape property
articleTitle: display_background_shape property
second_title: Aspose.Words for Python
description: "ViewOptions.display_background_shape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /zh/python-net/aspose.words.settings/viewoptions/display_background_shape/
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
# 使用 HTML 字符串创建具有纯色背景的新文档。
html = "<html>\n                <body style='background-color: blue'>\n                    <p>Hello world!</p>\n                </body>\n            </html>"
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.unicode())))
# 文档的来源具有纯色背景，
# 其存在将把 "DisplayBackgroundShape" 标志设置为 "true"。
self.assertTrue(doc.view_options.display_background_shape)
# 将 "DisplayBackgroundShape" 保持为 "true" 以使文档显示背景颜色。
# 这可能会影响某些文本颜色，以提高可见性。
# 将 "DisplayBackgroundShape" 设置为 "false" 以不显示背景颜色。
doc.view_options.display_background_shape = display_background_shape
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayBackgroundShape.docx')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

