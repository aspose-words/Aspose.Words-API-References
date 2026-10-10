---
title: FieldInclude.lock_fields property
linktitle: lock_fields property
articleTitle: lock_fields property
second_title: Aspose.Words for Python
description: "FieldInclude.lock_fields property. Gets or sets whether to prevent fields in the included document from being updated."
type: docs
weight: 30
url: /it/python-net/aspose.words.fields/fieldinclude/lock_fields/
---

## FieldInclude.lock_fields property

Gets or sets whether to prevent fields in the included document from being updated.


```python
@property
def lock_fields(self) -> bool:
    ...

@lock_fields.setter
def lock_fields(self, value: bool):
    ...

```

### Examples

Shows how to create an INCLUDE field, and set its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Possiamo usare un campo INCLUDE per importare una parte di un altro documento nel file system locale.
# Il segnalibro dell'altro documento a cui facciamo riferimento con questo campo contiene questa parte importata.
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

