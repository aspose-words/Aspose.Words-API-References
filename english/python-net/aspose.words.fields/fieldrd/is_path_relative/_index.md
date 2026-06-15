---
title: FieldRD.is_path_relative property
linktitle: is_path_relative property
articleTitle: is_path_relative property
second_title: Aspose.Words for Python
description: "FieldRD.is_path_relative property. Gets or sets whether the path is relative to the current document."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldrd/is_path_relative/
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
# Use a document builder to insert a table of contents,
# and then add one entry for the table of contents on the following page.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
builder.writeln('TOC entry from within this document')
# Insert an RD field, which references another local file system document in its FileName property.
# The TOC will also now accept all headings from the referenced document as entries for its table.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF_DOC, update_field=True).as_field_rd()
field.file_name = ARTIFACTS_DIR + 'ReferencedDocument.docx'
self.assertEqual(f' RD  {ARTIFACTS_DIR.replace(chr(92), chr(92) + chr(92))}ReferencedDocument.docx', field.get_field_code())
# Create the document that the RD field is referencing and insert a heading.
# This heading will show up as an entry in the TOC field in our first document.
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

