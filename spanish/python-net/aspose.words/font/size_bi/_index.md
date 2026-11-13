---
title: Font.size_bi property
linktitle: size_bi property
articleTitle: size_bi property
second_title: Aspose.Words for Python
description: "Font.size_bi property. Gets or sets the font size in points used in a right-to-left document."
type: docs
weight: 360
url: /es/python-net/aspose.words/font/size_bi/
---

## Font.size_bi property

Gets or sets the font size in points used in a right-to-left document.


```python
@property
def size_bi(self) -> float:
    ...

@size_bi.setter
def size_bi(self, value: float):
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

