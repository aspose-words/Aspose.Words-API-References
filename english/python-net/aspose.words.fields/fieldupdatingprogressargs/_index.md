---
title: FieldUpdatingProgressArgs class
linktitle: FieldUpdatingProgressArgs class
articleTitle: FieldUpdatingProgressArgs class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldUpdatingProgressArgs class. Provides data for the field updating progress event."
type: docs
weight: 1110
url: /python-net/aspose.words.fields/fieldupdatingprogressargs/
---

## FieldUpdatingProgressArgs class

Provides data for the field updating progress event.


### Properties

| Name | Description |
| --- | --- |
| [total_fields_count](./total_fields_count/) | Gets the total fields count to be updated. |
| [update_completed](./update_completed/) | Gets a value indicating whether field updating is completed. |
| [updated_fields_count](./updated_fields_count/) | Gets the number of updated fields. |

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

