---
title: Font.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "Font.bidi property. Specifies whether the contents of this run shall have right-to-left characteristics."
type: docs
weight: 30
url: /ru/python-net/aspose.words/font/bidi/
---

## Font.bidi property

Specifies whether the contents of this run shall have right-to-left characteristics.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

This property, when on, shall not be used with strongly left-to-right text. Any behavior under that condition is unspecified.
This property, when off, shall not be used with strong right-to-left text. Any behavior under that condition is unspecified.

When the contents of this run are displayed, all characters shall be treated as complex script characters for formatting
purposes. This means that [Font.bold_bi](../bold_bi/), [Font.italic_bi](../italic_bi/), [Font.size_bi](../size_bi/) and a corresponding font name
will be used when rendering this run.

Also, when the contents of this run are displayed, this property acts as a right-to-left override for characters
which are classified as "weak types" and "neutral types".




### Examples

Shows how to define separate sets of font settings for right-to-left, and right-to-left text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Определите набор параметров шрифта для текста слева направо.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# Определите другой набор параметров шрифта для текста справа налево.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# Мы можем использовать флаг "bidi", чтобы указать, будет ли добавляемый нами текст
# с помощью DocumentBuilder направлен справа налево. Когда мы добавляем текст с этим флагом, установленным в True,
# он будет отформатирован с использованием набора параметров шрифта для направления справа налево.
builder.font.bidi = True
builder.write('مرحبًا')
# Установите флаг в "False", а затем добавьте текст слева направо.
# Конструктор документа будет форматировать их, используя набор параметров шрифта слева направо.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

