---
title: FieldRD.is_path_relative property
linktitle: is_path_relative property
articleTitle: is_path_relative property
second_title: Aspose.Words for Python
description: "FieldRD.is_path_relative property. Gets or sets whether the path is relative to the current document."
type: docs
weight: 30
url: /es/python-net/aspose.words.fields/fieldrd/is_path_relative/
---

## FieldRD.is_path_relative property

Gets or sets whether the path is relative to the current document.


```python
@property
def is_path_relative(self) -> bool:
    ...

@is_path_relative.setter
def is_path_relative(self, value: bool):
    ...

```

### Examples

Shows to use the RD field to create a table of contents entries from headings in other documents.

```python
import aspose.words as aw
import test_util
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Utilice un document builder para insertar una tabla de contenidos,
# y luego añada una entrada para la tabla de contenidos en la página siguiente.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
builder.writeln('TOC entry from within this document')
# Inserte un campo RD, que hace referencia a otro documento del sistema de archivos local en su propiedad FileName.
# El TOC ahora también aceptará todos los encabezados del documento referenciado como entradas para su tabla.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF_DOC, update_field=True).as_field_rd()
field.file_name = ARTIFACTS_DIR + 'ReferencedDocument.docx'
self.assertEqual(f' RD  {ARTIFACTS_DIR.replace(chr(92), chr(92) + chr(92))}ReferencedDocument.docx', field.get_field_code())
# Cree el documento al que hace referencia el campo RD e inserte un encabezado.
# Este encabezado aparecerá como una entrada en el campo TOC de nuestro primer documento.
referenced_doc = aw.Document()
ref_doc_builder = aw.DocumentBuilder(doc=referenced_doc)
ref_doc_builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
ref_doc_builder.writeln('TOC entry from referenced document')
referenced_doc.save(file_name=ARTIFACTS_DIR + 'ReferencedDocument.docx')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.RD.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldRD](../)

