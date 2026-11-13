---
title: Font.name_bi property
linktitle: name_bi property
articleTitle: name_bi property
second_title: Aspose.Words for Python
description: "Font.name_bi property. Returns or sets the name of the font in a right-to-left language document."
type: docs
weight: 250
url: /es/python-net/aspose.words/font/name_bi/
---

## Font.name_bi property

Returns or sets the name of the font in a right-to-left language document.


```python
@property
def name_bi(self) -> str:
    ...

@name_bi.setter
def name_bi(self, value: str):
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
* property [Font.name](../name/)

