---
title: Font.name_other property
linktitle: name_other property
articleTitle: name_other property
second_title: Aspose.Words for Python
description: "Font.name_other property. Returns or sets the font used for characters with character codes from 128 through 255."
type: docs
weight: 270
url: /es/python-net/aspose.words/font/name_other/
---

## Font.name_other property

Returns or sets the font used for characters with character codes from 128 through 255.


```python
@property
def name_other(self) -> str:
    ...

@name_other.setter
def name_other(self, value: str):
    ...

```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Supongamos un run que usamos el generador para insertar mientras usamos esta configuración de fuente
# contiene caracteres dentro del rango de caracteres ASCII. En ese caso,
# mostrará esos caracteres usando esta fuente.
builder.font.name_ascii = 'Calibri'
# Al no especificarse otra fuente, el generador también aplicará esta fuente a todos los caracteres que inserte.
self.assertEqual('Calibri', builder.font.name)
# Especifique una fuente para usar con todos los caracteres fuera del rango ASCII.
# Idealmente, esta fuente debería tener un glifo para cada código de carácter no ASCII requerido.
builder.font.name_other = 'Courier New'
# Inserte un run con una palabra compuesta por caracteres ASCII, y una palabra con todos los caracteres fuera de ese rango.
# Cada carácter se mostrará usando una de las fuentes, dependiendo de.
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

