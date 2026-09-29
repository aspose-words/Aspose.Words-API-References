---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /tr/python-net/aspose.words/font/hidden/
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
# Hidden bayrağı true olarak ayarlandığında, bu Font nesnesiyle oluşturduğumuz tüm metin belgede görünmez olacaktır.
# Hidden text seçeneğini etkinleştirmediğimiz sürece gizli metni göremeyecek veya vurgulayamayacağız
# "File" -> "Options" -> "Display" yoluyla Microsoft Word'de bulunur. Metin hâlâ orada olacak,
# ve bu metne programlı olarak erişebileceğiz.
# Bu yöntemi hassas bilgileri gizlemek için kullanmanız önerilmez.
builder.font.hidden = True
builder.font.size = 36
builder.writeln('This text will not be visible in the document.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Hidden.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

