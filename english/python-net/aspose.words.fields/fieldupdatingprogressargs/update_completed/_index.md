---
title: FieldUpdatingProgressArgs.update_completed property
linktitle: update_completed property
articleTitle: update_completed property
second_title: Aspose.Words for Python
description: "FieldUpdatingProgressArgs.update_completed property. Gets a value indicating whether field updating is completed."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldupdatingprogressargs/update_completed/
---

## FieldUpdatingProgressArgs.update_completed property

Gets a value indicating whether field updating is completed.


```python
@property
def update_completed(self) -> bool:
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

