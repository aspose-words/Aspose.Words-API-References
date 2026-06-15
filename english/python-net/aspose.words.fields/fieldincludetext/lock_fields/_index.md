---
title: FieldIncludeText.lock_fields property
linktitle: lock_fields property
articleTitle: lock_fields property
second_title: Aspose.Words for Python
description: "FieldIncludeText.lock_fields property. Gets or sets whether to prevent fields in the included document from being updated."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldincludetext/lock_fields/
---

## FieldIncludeText.lock_fields property

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

