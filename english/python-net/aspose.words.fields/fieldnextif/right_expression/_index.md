---
title: FieldNextIf.right_expression property
linktitle: right_expression property
articleTitle: right_expression property
second_title: Aspose.Words for Python
description: "FieldNextIf.right_expression property. Gets or sets the right part of the comparison expression."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldnextif/right_expression/
---

## FieldNextIf.right_expression property

Gets or sets the right part of the comparison expression.


```python
@property
def right_expression(self) -> str:
    ...

@right_expression.setter
def right_expression(self, value: str):
    ...

```

### Examples

Shows how to use NEXT/NEXTIF fields to merge multiple rows into one page during a mail merge (InsertMergeFields).

```python
def insert_merge_fields(self, builder, first_field_text_before):
    self.insert_merge_field(builder, 'Courtesy Title', first_field_text_before, ' ')
    self.insert_merge_field(builder, 'First Name', None, ' ')
    self.insert_merge_field(builder, 'Last Name', None, None)
    builder.insert_paragraph()

def insert_merge_field(self, builder, field_name, text_before, text_after):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_MERGE_FIELD, update_field=True).as_field_merge_field()
    field.field_name = field_name
    field.text_before = text_before
    field.text_after = text_after
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldNextIf](../)

