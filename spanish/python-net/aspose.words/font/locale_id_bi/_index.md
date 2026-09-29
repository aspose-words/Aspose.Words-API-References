---
title: Font.locale_id_bi property
linktitle: locale_id_bi property
articleTitle: locale_id_bi property
second_title: Aspose.Words for Python
description: "Font.locale_id_bi property. Gets or sets the locale identifier (language) of the formatted right-to-left characters."
type: docs
weight: 210
url: /es/python-net/aspose.words/font/locale_id_bi/
---

## Font.locale_id_bi property

Gets or sets the locale identifier (language) of the formatted right-to-left characters.


```python
@property
def locale_id_bi(self) -> int:
    ...

@locale_id_bi.setter
def locale_id_bi(self, value: int):
    ...

```

### Remarks

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx


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

