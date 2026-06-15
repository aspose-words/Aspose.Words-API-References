---
title: IFieldUpdatingCallback.field_updating method
linktitle: field_updating method
articleTitle: field_updating method
second_title: Aspose.Words for Python
description: "IFieldUpdatingCallback.field_updating method. A user defined method that is called just before a field is updated."
type: docs
weight: 20
url: /python-net/aspose.words.fields/ifieldupdatingcallback/field_updating/
---

## field_updating(field) {#field}

A user defined method that is called just before a field is updated.


```python
def field_updating(self, field: aspose.words.fields.Field):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../field/) |  |

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
* class [IFieldUpdatingCallback](../)

