---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /ar/python-net/aspose.words/font/hidden/
---

## Font.hidden property

True if the font is formatted as hidden text.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Examples

Shows how to create a run of hidden text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# عند ضبط علامة Hidden على true، أي نص نقوم بإنشائه باستخدام كائن الخط هذا سيكون غير مرئي في المستند.
# لن نرى أو نُبرز النص المخفي إلا إذا فعلنا خيار \"النص المخفي\"
# الموجود في Microsoft Word عبر \"File\" -> \"Options\" -> \"Display\". سيظل النص موجودًا هناك،
# وسنتمكن من الوصول إلى هذا النص برمجيًا.
# لا يُنصح باستخدام هذه الطريقة لإخفاء المعلومات الحساسة.
builder.font.hidden = True
builder.font.size = 36
builder.writeln('This text will not be visible in the document.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Hidden.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

