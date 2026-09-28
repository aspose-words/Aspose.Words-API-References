---
title: Font.subscript property
linktitle: subscript property
articleTitle: subscript property
second_title: Aspose.Words for Python
description: "Font.subscript property. True if the font is formatted as subscript."
type: docs
weight: 440
url: /ar/python-net/aspose.words/font/subscript/
---

## Font.subscript property

True if the font is formatted as subscript.


```python
@property
def subscript(self) -> bool:
    ...

@subscript.setter
def subscript(self, value: bool):
    ...

```

### Examples

Shows how to format text to offset its position.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# ارفع هذا المقطع النصي 5 نقاط فوق الخط الأساسي.
run = aw.Run(doc=doc, text='Raised text. ')
run.font.position = 5
para.append_child(run)
# اخفض هذا المقطع النصي 10 نقاط تحت الخط الأساسي.
run = aw.Run(doc=doc, text='Lowered text. ')
run.font.position = -10
para.append_child(run)
# أضف مقطع نص عادي.
run = aw.Run(doc=doc, text='Text in its default position. ')
para.append_child(run)
# أضف مقطع نص يظهر كحرف سفلي.
run = aw.Run(doc=doc, text='Subscript. ')
run.font.subscript = True
para.append_child(run)
# أضف مقطع نص يظهر كحرف علوي.
run = aw.Run(doc=doc, text='Superscript.')
run.font.superscript = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.PositionSubscript.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

