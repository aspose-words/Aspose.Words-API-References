---
title: StructuredDocumentTag.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.id property. Specifies a unique read-only persistent numerical Id for this SDT."
type: docs
weight: 140
url: /es/python-net/aspose.words.markup/structureddocumenttag/id/
---

## StructuredDocumentTag.id property

Specifies a unique read-only persistent numerical Id for this **SDT**.




```python
@property
def id(self) -> int:
    ...

```

### Remarks

Id attribute shall follow these rules:

* The document shall retain SDT ids only if the whole document is cloned [Document.clone()](../../../aspose.words/document/clone/#bool).
  
* During [DocumentBase.import_node()](../../../aspose.words/documentbase/import_node/#node_bool)
  Id shall be retained if import does not cause conflicts with other SDT Ids in
  the target document.
  
* If multiple SDT nodes specify the same decimal number value for the Id attribute,
  then the first SDT in the document shall maintain this original Id,
  and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
  
* During standalone SDT Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener) operation new unique ID will be generated for the cloned SDT node.
  
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned
  to it when the document is loaded.
  





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

