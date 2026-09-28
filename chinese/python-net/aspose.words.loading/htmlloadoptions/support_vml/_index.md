---
title: HtmlLoadOptions.support_vml property
linktitle: support_vml property
articleTitle: support_vml property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.support_vml property. Gets or sets a value indicating whether to support VML images."
type: docs
weight: 70
url: /zh/python-net/aspose.words.loading/htmlloadoptions/support_vml/
---

## HtmlLoadOptions.support_vml property

Gets or sets a value indicating whether to support VML images.


```python
@property
def support_vml(self) -> bool:
    ...

@support_vml.setter
def support_vml(self, value: bool):
    ...

```

### Examples

Shows how to support conditional comments while loading an HTML document.

```python
load_options = aw.loading.HtmlLoadOptions()
# 如果该值为 true，则在解析加载的文档时会考虑 VML 代码。
load_options.support_vml = support_vml
# 此文档在 "<!--[if gte vml 1]>" 标记中包含 JPEG 图像，
# 并且在 "<![if !vml]>" 标记中包含另一个 PNG 图像。
# 如果我们将 "SupportVml" 标志设置为 "true"，则 Aspose.Words 将加载 JPEG。
# 如果我们将此标志设置为 "false"，则 Aspose.Words 将仅加载 PNG。
doc = aw.Document(file_name=MY_DIR + 'VML conditional.htm', load_options=load_options)
if support_vml:
    self.assertEqual(aw.drawing.ImageType.JPEG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
else:
    self.assertEqual(aw.drawing.ImageType.PNG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

