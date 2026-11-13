---
title: Font.small_caps property
linktitle: small_caps property
articleTitle: small_caps property
second_title: Aspose.Words for Python
description: "Font.small_caps property. True if the font is formatted as small capital letters."
type: docs
weight: 370
url: /es/python-net/aspose.words/font/small_caps/
---

## Font.small_caps property

True if the font is formatted as small capital letters.


```python
@property
def small_caps(self) -> bool:
    ...

@small_caps.setter
def small_caps(self, value: bool):
    ...

```

### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# Hay dos formas de lograr que un run muestre su texto en minúsculas en mayúsculas sin cambiar el contenido.
# 1 -  Establezca la bandera AllCaps para mostrar todos los caracteres en mayúsculas regulares:
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 -  Establezca la bandera SmallCaps para mostrar todos los caracteres en pequeñas mayúsculas:
# Si un carácter está en minúscula, aparecerá en su forma mayúscula
# pero tendrá la misma altura que la minúscula (la x-height de la fuente).
# Los caracteres que estaban originalmente en mayúscula se verán iguales.
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

