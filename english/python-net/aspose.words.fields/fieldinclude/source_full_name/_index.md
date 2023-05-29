---
title: FieldInclude.source_full_name property
linktitle: source_full_name property
articleTitle: source_full_name property
second_title: Aspose.Words for Python
description: "FieldInclude.source_full_name property. Gets or sets the location of the document."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldinclude/source_full_name/
---

## FieldInclude.source_full_name property

Gets or sets the location of the document.


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

