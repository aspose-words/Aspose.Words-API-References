---
title: Font.emboss property
linktitle: emboss property
articleTitle: emboss property
second_title: Aspose.Words for Python
description: "Font.emboss property. True if the font is formatted as embossed."
type: docs
weight: 100
url: /ar/python-net/aspose.words/font/emboss/
---

## Font.emboss property

True if the font is formatted as embossed.


```python
@property
def emboss(self) -> bool:
    ...

@emboss.setter
def emboss(self, value: bool):
    ...

```

### Examples

Shows how to apply engraving/embossing effects to text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 36
builder.font.color = aspose.pydrawing.Color.light_blue
# فيما يلي طريقتان لاستخدام الظلال لتطبيق تأثير ثلاثي الأبعاد على النص.
# 1 - نقش النص لجعله يبدو كأن الحروف غارقة في الصفحة:
builder.font.engrave = True
builder.writeln('This text is engraved.')
# 2 - بروز النص لجعله يبدو كأن الحروف تبرز من الصفحة:
builder.font.engrave = False
builder.font.emboss = True
builder.writeln('This text is embossed.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.EngraveEmboss.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

