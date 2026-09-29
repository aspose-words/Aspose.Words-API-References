---
title: ImportFormatOptions.keep_source_numbering property
linktitle: keep_source_numbering property
articleTitle: keep_source_numbering property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.keep_source_numbering property. Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents"
type: docs
weight: 70
url: /es/python-net/aspose.words/importformatoptions/keep_source_numbering/
---

## ImportFormatOptions.keep_source_numbering property

Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and
destination documents.
The default value is ``False``.



```python
@property
def keep_source_numbering(self) -> bool:
    ...

@keep_source_numbering.setter
def keep_source_numbering(self, value: bool):
    ...

```

### Examples

Shows how to import a document with numbered lists.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List source.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List destination.docx')
self.assertEqual(4, dst_doc.lists.count)
options = aw.ImportFormatOptions()
# Si hay un conflicto de estilos de lista, aplique el formato de lista del documento fuente.
# Establezca la propiedad "KeepSourceNumbering" en "false" para no importar ningún número de lista al documento de destino.
# Establezca la propiedad "KeepSourceNumbering" a "true" para importar todo lo que entra en conflicto
# Enumeración de estilo de lista con la misma apariencia que tenía en el documento de origen.
options.keep_source_numbering = is_keep_source_numbering
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options)
dst_doc.update_list_labels()
self.assertEqual(5 if is_keep_source_numbering else 4, dst_doc.lists.count)
```

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List with the same definition identifier - source.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List with the same definition identifier - destination.docx')
# Establezca la propiedad "KeepSourceNumbering" a "true" para aplicar un ID de definición de lista diferente
# a estilos idénticos como Aspose.Words los importa en los documentos de destino.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = True
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options=import_format_options)
dst_doc.update_list_labels()
```

Shows how to resolve list numbering clashes in source and destination documents.

```python
# Abra un documento con un esquema de numeración de lista personalizado y luego clónelo.
# Dado que ambos tienen el mismo formato de numeración, los formatos chocarán si importamos un documento en el otro.
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# Cuando importamos el clon del documento al original y luego lo añadimos,
# entonces las dos listas con el mismo formato de lista se unirán.
# Si establecemos la bandera "KeepSourceNumbering" a "false", entonces la lista del clon del documento
# que añadimos al original continuará con la numeración de la lista a la que la añadimos.
# Esto fusionará efectivamente las dos listas en una.
# Si establecemos la bandera "KeepSourceNumbering" a "true", entonces el clon del documento
# la lista conservará su numeración original, haciendo que las dos listas aparezcan como listas separadas.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = keep_source_numbering
importer = aw.NodeImporter(src_doc=src_doc, dst_doc=dst_doc, import_format_mode=aw.ImportFormatMode.KEEP_DIFFERENT_STYLES, import_format_options=import_format_options)
for paragraph in src_doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    imported_node = importer.import_node(paragraph, True)
    dst_doc.first_section.body.append_child(imported_node)
dst_doc.update_list_labels()
if keep_source_numbering:
    self.assertEqual('6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4\r\n' + '6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4', dst_doc.first_section.body.to_string(save_format=aw.SaveFormat.TEXT).strip())
else:
    self.assertEqual('6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4\r\n' + '10. Item 1\r\n' + '11. Item 2 \r\n' + '12. Item 3\r\n' + '13. Item 4', dst_doc.first_section.body.to_string(save_format=aw.SaveFormat.TEXT).strip())
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

