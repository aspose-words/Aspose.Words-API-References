---
title: FieldInclude.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldInclude.bookmark_name property. Gets or sets the name of the bookmark in the document to include."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldinclude/bookmark_name/
---

## FieldInclude.bookmark_name property

Gets or sets the name of the bookmark in the document to include.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to create an INCLUDE field, and set its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Wir können ein INCLUDE-Feld verwenden, um einen Teil eines anderen Dokuments im lokalen Dateisystem zu importieren.
# Das Lesezeichen aus dem anderen Dokument, das wir mit diesem Feld referenzieren, enthält diesen importierten Teil.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INCLUDE, update_field=True).as_field_include()
field.source_full_name = MY_DIR + 'Bookmarks.docx'
field.bookmark_name = 'MyBookmark1'
field.lock_fields = False
field.text_converter = 'Microsoft Word'
assert re.search(' INCLUDE .* MyBookmark1 \\\\\\\\c \\"Microsoft Word\\"', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INCLUDE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldInclude](../)

