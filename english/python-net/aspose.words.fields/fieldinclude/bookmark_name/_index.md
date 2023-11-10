---
title: FieldInclude.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldInclude.bookmark_name property. Gets or sets the name of the bookmark in the document to include."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldinclude/bookmark_name/
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
builder = aw.DocumentBuilder(doc)

# We can use an INCLUDE field to import a portion of another document in the local file system.
# The bookmark from the other document that we reference with this field contains this imported portion.
field = builder.insert_field(aw.fields.FieldType.FIELD_INCLUDE, True).as_field_include()
field.source_full_name = MY_DIR + "Bookmarks.docx"
field.bookmark_name = "MyBookmark1"
field.lock_fields = False
field.text_converter = "Microsoft Word"

self.assertRegex(field.get_field_code(), r' INCLUDE .* MyBookmark1 \\c "Microsoft Word"')

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_include.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldInclude](../)

