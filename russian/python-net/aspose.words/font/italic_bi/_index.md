---
title: Font.italic_bi property
linktitle: italic_bi property
articleTitle: italic_bi property
second_title: Aspose.Words for Python
description: "Font.italic_bi property. True if the right-to-left text is formatted as italic."
type: docs
weight: 170
url: /ru/python-net/aspose.words/font/italic_bi/
---

## Font.italic_bi property

True if the right-to-left text is formatted as italic.


```python
@property
def italic_bi(self) -> bool:
    ...

@italic_bi.setter
def italic_bi(self, value: bool):
    ...

```

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

