---
title: Font.bold_bi property
linktitle: bold_bi property
articleTitle: bold_bi property
second_title: Aspose.Words for Python
description: "Font.bold_bi property. True if the right-to-left text is formatted as bold."
type: docs
weight: 50
url: /tr/python-net/aspose.words/font/bold_bi/
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
# Soldan sağa metin için bir dizi yazı tipi ayarı tanımlayın.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# Sağdan sola metin için başka bir yazı tipi ayarı seti tanımlayın.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# "bidi" bayrağını, ekleyeceğimiz metnin
# belge oluşturucu ile sağdan sola olup olmadığını belirtmek için kullanabiliriz. Bu bayrak True olarak ayarlandığında metin eklediğimizde,
# metin sağdan sola yazı tipi ayar seti kullanılarak biçimlendirilecektir.
builder.font.bidi = True
builder.write('مرحبًا')
# Bayrağı "False" olarak ayarlayın ve ardından soldan sağa metin ekleyin.
# Belge oluşturucu, bunları soldan sağa ayarlanmış yazı tipi ayarlarıyla biçimlendirecek.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

