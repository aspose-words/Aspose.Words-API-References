---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /es/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
---

## StructuredDocumentTag.is_temporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents
are modified.



```python
@property
def is_temporary(self) -> bool:
    ...

@is_temporary.setter
def is_temporary(self, value: bool):
    ...

```

### Examples

Shows how to make single-use controls.

```python
doc = aw.Document()
# Inserte una etiqueta de documento estructurado de texto plano,
# que actuará como un formulario de texto plano en el que el usuario podrá introducir texto.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Establezca la propiedad "IsTemporary" a "true" para que la etiqueta de documento estructurado desaparezca y
# asimile su contenido en el documento después de que el usuario lo edite una vez en Microsoft Word.
# Establezca la propiedad "IsTemporary" a "false" para permitir que el usuario edite el contenido
# de la etiqueta de documento estructurado cualquier número de veces.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# Inserte otra etiqueta de documento estructurado en forma de casilla de verificación y establezca su estado predeterminado a "checked".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# Establezca la propiedad "IsTemporary" a "true" para que la casilla de verificación se convierta en un símbolo
# una vez que el usuario haga clic en ella en Microsoft Word.
# Establezca la propiedad "IsTemporary" a "false" para permitir que el usuario haga clic en la casilla de verificación cualquier número de veces.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

