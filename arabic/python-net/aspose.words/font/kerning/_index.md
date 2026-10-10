---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /ar/python-net/aspose.words/font/kerning/
---

## Font.kerning property

Gets or sets the font size at which kerning starts.


```python
@property
def kerning(self) -> float:
    ...

@kerning.setter
def kerning(self, value: float):
    ...

```

### Examples

Shows how to specify the font size at which kerning begins to take effect.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial Black'
# حدد حجم خط المنشئ، والحجم الأدنى الذي سيبدأ فيه تطبيق الكيرنينغ.
# حجم الخط ينخفض تحت عتبة الكيرنينغ، لذا فإن المقطع أدناه لن يحتوي على كيرنينغ.
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# حدد عتبة الكيرنينغ بحيث يكون حجم خط المنشئ الحالي أعلى منها.
# أي نص نضيفه من هذه النقطة سيُطبق عليه الكيرنينغ. المسافات بين الأحرف
# ستُضبط، مما ينتج عادةً مقطع نص أكثر جماليةً قليلاً.
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

