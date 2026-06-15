---
title: IFieldUpdatingProgressCallback class
linktitle: IFieldUpdatingProgressCallback class
articleTitle: IFieldUpdatingProgressCallback class
second_title: Aspose.Words for Python
description: "aspose.words.fields.IFieldUpdatingProgressCallback class. Implement this interface if you want to track field updating progress."
type: docs
weight: 1270
url: /python-net/aspose.words.fields/ifieldupdatingprogresscallback/
---

## IFieldUpdatingProgressCallback class

Implement this interface if you want to track field updating progress.


### Methods

| Name | Description |
| --- | --- |
|[ notify(args)](./notify/#fieldupdatingprogressargs) | A user defined method that is called when updating progress is changed. |

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

