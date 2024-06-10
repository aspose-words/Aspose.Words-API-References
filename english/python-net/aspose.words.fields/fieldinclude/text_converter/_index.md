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
builder = aw.DocumentBuilder(doc)
# We can use an INCLUDE field to import a portion of another document in the local file system.
# The bookmark from the other document that we reference with this field contains this imported portion.
field = builder.insert_field(aw.fields.FieldType.FIELD_INCLUDE, True).as_field_include()
field.source_full_name = MY_DIR + 'Bookmarks.docx'
field.bookmark_name = 'MyBookmark1'
field.lock_fields = False
field.text_converter = 'Microsoft Word'
self.assertRegex(field.get_field_code(), ' INCLUDE .* MyBookmark1 \\\\c "Microsoft Word"')
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_include.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldInclude](../)

