---
title: ControlChar.CR property
linktitle: CR property
articleTitle: CR property
second_title: Aspose.Words for Python
description: "ControlChar.CR property. Carriage return character: \\x000d or \\r"
type: docs
weight: 50
url: /tr/python-net/aspose.words/controlchar/CR/
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
# DocumentBuilder ile metin içeren paragraflar ekleyin.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# Belgeyi metin biçimine dönüştürmek, kontrol karakterlerinin
# belgenin bazı yapısal öğelerini, örneğin sayfa sonlarını temsil ettiğini gösterir.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + f'Hello again!{aw.ControlChar.CR}' + aw.ControlChar.PAGE_BREAK, doc.get_text())
# Bir belgeyi dize biçimine dönüştürürken,
# Trim yöntemiyle bazı kontrol karakterlerini atlayabiliriz.
self.assertEqual(f'Hello world!{aw.ControlChar.CR}' + 'Hello again!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [ControlChar](../)

