---
title: Font.name_ascii property
linktitle: name_ascii property
articleTitle: name_ascii property
second_title: Aspose.Words for Python
description: "Font.name_ascii property. Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127)."
type: docs
weight: 240
url: /tr/python-net/aspose.words/font/name_ascii/
---

## Font.name_ascii property

Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127).


```python
@property
def name_ascii(self) -> str:
    ...

@name_ascii.setter
def name_ascii(self, value: str):
    ...

```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bu yazı tipi yapılandırmasını kullanarak oluşturucunun eklediği bir koşu olduğunu varsayalım
# ASCII karakter aralığı içinde karakterler içerir. Bu durumda,
# Bu karakterleri bu yazı tipini kullanarak görüntüler.
builder.font.name_ascii = 'Calibri'
# Başka bir yazı tipi belirtilmediğinde, oluşturucu bu yazı tipini eklediği tüm karakterlere de uygular.
self.assertEqual('Calibri', builder.font.name)
# ASCII aralığının dışındaki tüm karakterler için kullanılacak bir yazı tipi belirtin.
# İdeal olarak, bu yazı tipinin gerekli her bir non-ASCII karakter kodu için bir glifi olmalıdır.
builder.font.name_other = 'Courier New'
# ASCII karakterlerden oluşan bir kelime ve bu aralığın dışındaki tüm karakterlerden oluşan bir kelime içeren bir koşul ekleyin.
# Her karakter, duruma bağlı olarak bu iki yazı tipinden biri kullanılarak görüntülenecek.
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

