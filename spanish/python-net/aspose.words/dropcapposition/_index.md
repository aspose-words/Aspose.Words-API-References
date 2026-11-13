---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /es/python-net/aspose.words/dropcapposition/
---

## DropCapPosition enumeration

Specifies the position for a drop cap text.


### Members

| Name | Description |
| --- | --- |
| NONE | The paragraph does not have a drop cap. |
| NORMAL | The drop cap is positioned inside the text margin on the anchor paragraph. |
| MARGIN | The drop cap is positioned outside the text margin on the anchor paragraph. |

### Examples

Shows how to create a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte un párrafo con una letra grande con la que comienza el texto en los segundo y tercer párrafos.
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# Actualmente, los segundo y tercer párrafos aparecerán debajo del primero.
# Podemos convertir el primer párrafo en una letra capitular para los demás párrafos mediante su objeto "ParagraphFormat".
# Establezca la propiedad "DropCapPosition" a "DropCapPosition.Margin" para colocar la letra capitular
# fuera del margen izquierdo de la página si nuestro texto es de izquierda a derecha.
# Establezca la propiedad "DropCapPosition" a "DropCapPosition.Normal" para colocar la letra capitular dentro de los márgenes de la página
# y para que el resto del texto fluya a su alrededor.
# "DropCapPosition.None" es el estado predeterminado para todos los párrafos.
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

