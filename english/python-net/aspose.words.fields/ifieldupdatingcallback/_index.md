---
title: IFieldUpdatingCallback class
linktitle: IFieldUpdatingCallback class
articleTitle: IFieldUpdatingCallback class
second_title: Aspose.Words for Python
description: "aspose.words.fields.IFieldUpdatingCallback class. Implement this interface if you want to have your own custom methods called during a field update."
type: docs
weight: 1260
url: /python-net/aspose.words.fields/ifieldupdatingcallback/
---

## IFieldUpdatingCallback class

Implement this interface if you want to have your own custom methods called during a field update.


### Methods

| Name | Description |
| --- | --- |
|[ field_updated(field)](./field_updated/#field) | A user defined method that is called just after a field is updated. |
|[ field_updating(field)](./field_updating/#field) | A user defined method that is called just before a field is updated. |

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

* module [aspose.words.fields](../)

