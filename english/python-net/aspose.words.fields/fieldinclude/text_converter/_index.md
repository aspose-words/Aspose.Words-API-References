---
title: FieldInclude.text_converter property
linktitle: text_converter property
articleTitle: text_converter property
second_title: Aspose.Words for Python
description: "FieldInclude.text_converter property. Gets or sets the name of the text converter for the format of the included file."
type: docs
weight: 50
url: /python-net/aspose.words.fields/fieldinclude/text_converter/
---

## FieldInclude.text_converter property

Gets or sets the name of the text converter for the format of the included file.


```python
@property
def text_converter(self) -> str:
    ...

@text_converter.setter
def text_converter(self, value: str):
    ...

```

### Examples

Shows how to create an INCLUDE field, and set its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# We can use an INCLUDE field to import a portion of another document in the local file system.
# The bookmark from the other document that we reference with this field contains this imported portion.
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

