---
title: HtmlLoadOptions.support_vml property
linktitle: support_vml property
articleTitle: support_vml property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.support_vml property. Gets or sets a value indicating whether to support VML images."
type: docs
weight: 70
url: /ar/python-net/aspose.words.loading/htmlloadoptions/support_vml/
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
# إذا كانت القيمة true، فإننا نأخذ كود VML في الاعتبار أثناء تحليل المستند المحمّل.
load_options.support_vml = support_vml
# هذا المستند يحتوي على صورة JPEG داخل وسوم "<!--[if gte vml 1]>" ،
# و صورة PNG مختلفة داخل وسوم "<![if !vml]>".
# إذا قمنا بتعيين العلامة "SupportVml" إلى "true"، فستقوم Aspose.Words بتحميل صورة JPEG.
# إذا قمنا بتعيين هذه العلامة إلى "false"، فستقوم Aspose.Words بتحميل صورة PNG فقط.
doc = aw.Document(file_name=MY_DIR + 'VML conditional.htm', load_options=load_options)
if support_vml:
    self.assertEqual(aw.drawing.ImageType.JPEG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
else:
    self.assertEqual(aw.drawing.ImageType.PNG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

