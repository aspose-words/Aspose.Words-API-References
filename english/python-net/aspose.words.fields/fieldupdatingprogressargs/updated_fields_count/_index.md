---
title: FieldUpdatingProgressArgs.updated_fields_count property
linktitle: updated_fields_count property
articleTitle: updated_fields_count property
second_title: Aspose.Words for Python
description: "FieldUpdatingProgressArgs.updated_fields_count property. Gets the number of updated fields."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldupdatingprogressargs/updated_fields_count/
---

## FieldUpdatingProgressArgs.updated_fields_count property

Gets the number of updated fields.


```python
@property
def updated_fields_count(self) -> int:
    ...

```

### Examples

Shows how to use callback methods during a field update (FieldUpdatingCallback).

```python
class FieldUpdatingCallback(aw.fields.IFieldUpdatingCallback, aw.fields.IFieldUpdatingProgressCallback):

    @property
    def field_updated_calls(self):
        pass

    def __init__(self):
        field_updated_calls = []

    def field_updating(self, field):
        if field.type == aw.fields.FieldType.FIELD_AUTHOR:
            field_author = field.as_field_author()
            field_author.author_name = 'Updating John Doe'

    def field_updated(self, field):
        field_updated_calls.append(field.result)

    def notify(self, args):
        print(f'{args.update_completed}/{args.total_fields_count}')
        print(f'{args.updated_fields_count}')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUpdatingProgressArgs](../)

