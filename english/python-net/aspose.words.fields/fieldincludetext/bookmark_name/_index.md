---
title: FieldIncludeText.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldIncludeText.bookmark_name property. Gets or sets the name of the bookmark in the document to include."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldincludetext/bookmark_name/
---

## FieldIncludeText.bookmark_name property

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

Shows how to create an INCLUDETEXT field, and set its properties (CreateFieldIncludeText).

```python
def create_field_include_text(self, builder, source_full_name, lock_fields, mime_type, text_converter, encoding):
    field_include_text = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INCLUDE_TEXT, update_field=True).as_field_include_text()
    field_include_text.source_full_name = source_full_name
    field_include_text.lock_fields = lock_fields
    field_include_text.mime_type = mime_type
    field_include_text.text_converter = text_converter
    field_include_text.encoding = encoding
    return field_include_text
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIncludeText](../)

