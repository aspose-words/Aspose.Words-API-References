---
title: StructuredDocumentTag.level property
linktitle: level property
articleTitle: level property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.level property. Gets the level at which this SDT occurs in the document tree."
type: docs
weight: 170
url: /es/python-net/aspose.words.markup/structureddocumenttag/level/
---

## StructuredDocumentTag.level property

Gets the level at which this **SDT** occurs in the document tree.



```python
@property
def level(self) -> aspose.words.markup.MarkupLevel:
    ...

```

### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# Cree una etiqueta de documento estructurado que contendrá texto plano.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Establezca el título y el color del marco que aparece al pasar el mouse sobre la etiqueta de documento estructurado en Microsoft Word.
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# Establezca una etiqueta para esta etiqueta de documento estructurado, que es obtenible
# como un elemento XML llamado "tag", con la cadena siguiente en su atributo "@val".
tag.tag = 'MyPlainTextSDT'
# Cada etiqueta de documento estructurado tiene un ID único aleatorio.
self.assertTrue(tag.id > 0)
# Establezca la fuente para el texto dentro de la etiqueta de documento estructurado.
tag.contents_font.name = 'Arial'
# Establezca la fuente para el texto al final de la etiqueta de documento estructurado.
# Cualquier texto que escribamos en el cuerpo del documento después de salir de la etiqueta con las teclas de flecha usará esta fuente.
tag.end_character_font.name = 'Arial Black'
# Por defecto, esto es falso y al presionar Enter mientras está dentro de una etiqueta de documento estructurado no ocurre nada.
# Cuando se establece en verdadero, nuestra etiqueta de documento estructurado puede tener varias líneas.
# Establezca la propiedad "Multiline" en "false" para permitir solo el contenido
# de esta etiqueta de documento estructurado que abarque una sola línea.
# Establezca la propiedad "Multiline" en "true" para permitir que la etiqueta contenga varias líneas de contenido.
tag.multiline = True
# Establezca la propiedad "Appearance" en "SdtAppearance.Tags" para mostrar etiquetas alrededor del contenido.
# Por defecto, la etiqueta de documento estructurado se muestra como BoundingBox.
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# Inserte un clon de nuestra etiqueta de documento estructurado en un nuevo párrafo.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# Utilice el método "RemoveSelfOnly" para eliminar una etiqueta de documento estructurado, manteniendo su contenido en el documento.
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

