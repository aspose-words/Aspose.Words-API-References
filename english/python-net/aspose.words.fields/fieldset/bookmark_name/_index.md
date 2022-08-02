---
title: bookmark_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the name of the bookmark."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldset/bookmark_name/
---

## FieldSet.bookmark_name property

Gets or sets the name of the bookmark.


### Examples

Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Name bookmarked text with a SET field.
# This field refers to the "bookmark" not a bookmark structure that appears within the text, but a named variable.
field_set = builder.insert_field(aw.fields.FieldType.FIELD_SET, False).as_field_set()
field_set.bookmark_name = "MyBookmark"
field_set.bookmark_text = "Hello world!"
field_set.update()

self.assertEqual(" SET  MyBookmark \"Hello world!\"", field_set.get_field_code())

# Refer to the bookmark by name in a REF field and display its contents.
field_ref = builder.insert_field(aw.fields.FieldType.FIELD_REF, True).as_field_ref()
field_ref.bookmark_name = "MyBookmark"
field_ref.update()

self.assertEqual(" REF  MyBookmark", field_ref.get_field_code())
self.assertEqual("Hello world!", field_ref.result)

doc.save(ARTIFACTS_DIR + "Field.field_set_ref.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSet](../)

