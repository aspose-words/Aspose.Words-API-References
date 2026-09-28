---
title: Font.bold_bi property
linktitle: bold_bi property
articleTitle: bold_bi property
second_title: Aspose.Words for Python
description: "Font.bold_bi property. True if the right-to-left text is formatted as bold."
type: docs
weight: 50
url: /ar/python-net/aspose.words/font/bold_bi/
---

## Font.bold_bi property

True if the right-to-left text is formatted as bold.


```python
@property
def bold_bi(self) -> bool:
    ...

@bold_bi.setter
def bold_bi(self, value: bool):
    ...

```

### Examples

Shows how to define separate sets of font settings for right-to-left, and right-to-left text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# عرّف مجموعة من إعدادات الخط للنص من اليسار إلى اليمين.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# عرّف مجموعة أخرى من إعدادات الخط للنص من اليمين إلى اليسار.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# يمكننا استخدام العلامة "bidi" لتحديد ما إذا كان النص الذي سنضيفه
# مع DocumentBuilder من اليمين إلى اليسار. عندما نضيف نصًا مع تعيين هذه العلامة إلى True،
# سيتم تنسيقه باستخدام مجموعة إعدادات الخط من اليمين إلى اليسار.
builder.font.bidi = True
builder.write('مرحبًا')
# قم بتعيين العلامة إلى "False"، ثم أضف نصًا من اليسار إلى اليمين.
# سوف يقوم منشئ المستند بتنسيق هذه باستخدام مجموعة إعدادات الخط من اليسار إلى اليمين.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

