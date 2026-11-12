---
title: HtmlLoadOptions.support_vml property
linktitle: support_vml property
articleTitle: support_vml property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.support_vml property. Gets or sets a value indicating whether to support VML images."
type: docs
weight: 70
url: /ru/python-net/aspose.words.loading/htmlloadoptions/support_vml/
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
# Если значение равно true, то мы учитываем код VML при разборе загруженного документа.
load_options.support_vml = support_vml
# Этот документ содержит изображение JPEG внутри тегов "<!--[if gte vml 1]>" ,
# и другое изображение PNG внутри тегов "<![if !vml]>".
# Если мы установим флаг "SupportVml" в значение "true", то Aspose.Words загрузит JPEG.
# Если мы установим этот флаг в значение "false", то Aspose.Words загрузит только PNG.
doc = aw.Document(file_name=MY_DIR + 'VML conditional.htm', load_options=load_options)
if support_vml:
    self.assertEqual(aw.drawing.ImageType.JPEG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
else:
    self.assertEqual(aw.drawing.ImageType.PNG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

