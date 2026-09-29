---
title: HtmlLoadOptions.support_vml property
linktitle: support_vml property
articleTitle: support_vml property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.support_vml property. Gets or sets a value indicating whether to support VML images."
type: docs
weight: 70
url: /sv/python-net/aspose.words.loading/htmlloadoptions/support_vml/
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
# Om värdet är true tar vi VML‑kod i beaktande när vi parsar det inlästa dokumentet.
load_options.support_vml = support_vml
# Detta dokument innehåller en JPEG-bild inom "<!--[if gte vml 1]>"-taggar,
# och en annan PNG-bild inom "<![if !vml]>"-taggar.
# Om vi sätter flaggan "SupportVml" till "true", kommer Aspose.Words att ladda JPEG‑bilden.
# Om vi sätter den här flaggan till "false", kommer Aspose.Words endast att ladda PNG‑bilden.
doc = aw.Document(file_name=MY_DIR + 'VML conditional.htm', load_options=load_options)
if support_vml:
    self.assertEqual(aw.drawing.ImageType.JPEG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
else:
    self.assertEqual(aw.drawing.ImageType.PNG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

