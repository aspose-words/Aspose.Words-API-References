---
title: StructuredDocumentTag.is_showing_placeholder_text property
linktitle: is_showing_placeholder_text property
articleTitle: is_showing_placeholder_text property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_showing_placeholder_text property. Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT)."
type: docs
weight: 150
url: /es/python-net/aspose.words.markup/structureddocumenttag/is_showing_placeholder_text/
---

## StructuredDocumentTag.is_showing_placeholder_text property

Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text
(as opposed to regular text contents within the SDT).


if set to ``True``, this state shall be resumed (showing placeholder text) upon opening this document.





```python
@property
def is_showing_placeholder_text(self) -> bool:
    ...

@is_showing_placeholder_text.setter
def is_showing_placeholder_text(self, value: bool):
    ...

```

### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# Inserte una etiqueta de documento estructurado de texto plano del tipo "PlainText", que funcionará como un cuadro de texto.
# El contenido que mostrará por defecto es un mensaje "Click here to enter text.".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Podemos hacer que la etiqueta muestre el contenido de un bloque de construcción en lugar del texto predeterminado.
# Primero, agregue un bloque de construcción con contenido al documento de glosario.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# Luego, use la propiedad "PlaceholderName" de la etiqueta de documento estructurado para referenciar ese bloque de construcción por su nombre.
tag.placeholder_name = 'Custom Placeholder'
# Si "PlaceholderName" se refiere a un bloque existente en el documento de glosario del documento principal,
# podremos verificar el bloque de construcción mediante la propiedad "Placeholder".
self.assertEqual(substitute_block, tag.placeholder)
# Establezca la propiedad "IsShowingPlaceholderText" en "true" para tratar el
# contenido actual de la etiqueta de documento estructurado como texto de marcador de posición.
# Esto significa que al hacer clic en el cuadro de texto en Microsoft Word se resaltará inmediatamente todo el contenido de la etiqueta.
# Establezca la propiedad "IsShowingPlaceholderText" en "false" para obtener el
# etiqueta de documento estructurado para tratar su contenido como texto que ya ha ingresado el usuario.
# Al hacer clic en este texto en Microsoft Word se colocará el cursor intermitente en la ubicación pulsada.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

