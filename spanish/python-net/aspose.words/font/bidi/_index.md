---
title: Font.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "Font.bidi property. Specifies whether the contents of this run shall have right-to-left characteristics."
type: docs
weight: 30
url: /es/python-net/aspose.words/font/bidi/
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
# Defina un conjunto de configuraciones de fuente para texto de izquierda a derecha.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# Defina otro conjunto de configuraciones de fuente para texto de derecha a izquierda.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# Podemos usar la bandera "bidi" para indicar si el texto que estamos a punto de agregar
# con el DocumentBuilder es de derecha a izquierda. Cuando agregamos texto con esta bandera establecida en True,
# se formateará usando el conjunto de configuraciones de fuente de derecha a izquierda.
builder.font.bidi = True
builder.write('مرحبًا')
# Establezca la bandera a "False", y luego añada texto de izquierda a derecha.
# El generador de documentos formateará estos usando el conjunto de configuraciones de fuente de izquierda a derecha.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

