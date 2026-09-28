---
title: ControlChar.CR property
linktitle: CR property
articleTitle: CR property
second_title: Aspose.Words for Python
description: "ControlChar.CR property. Carriage return character: \\x000d or \\r"
type: docs
weight: 50
url: /ar/python-net/aspose.words/controlchar/CR/
---

## ControlChar.CR property

Carriage return character: "\\x000d" or "\\r". Same as [ControlChar.PARAGRAPH_BREAK](../PARAGRAPH_BREAK/).



```python
@property
def CR(self) -> str:
    ...

```

### Examples

Shows how to use control characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج فقرات بنص باستخدام DocumentBuilder.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# تحويل المستند إلى صيغة نصية يكشف أن الأحرف التحكمية
# تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + f'Hello again!{aw.ControlChar.CR}' + aw.ControlChar.PAGE_BREAK, doc.get_text())
# عند تحويل مستند إلى صيغة سلسلة،
# يمكننا حذف بعض الأحرف التحكمية باستخدام طريقة Trim.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + 'Hello again!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [ControlChar](../)

