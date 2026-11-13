---
title: Font.bold_bi property
linktitle: bold_bi property
articleTitle: bold_bi property
second_title: Aspose.Words for Python
description: "Font.bold_bi property. True if the right-to-left text is formatted as bold."
type: docs
weight: 50
url: /es/python-net/aspose.words/font/bold_bi/
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

