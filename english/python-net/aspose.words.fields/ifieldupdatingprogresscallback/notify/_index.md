---
title: IFieldUpdatingProgressCallback.notify method
linktitle: notify method
articleTitle: notify method
second_title: Aspose.Words for Python
description: "IFieldUpdatingProgressCallback.notify method. A user defined method that is called when updating progress is changed."
type: docs
weight: 10
url: /python-net/aspose.words.fields/ifieldupdatingprogresscallback/notify/
---

## notify(args) {#fieldupdatingprogressargs}

A user defined method that is called when updating progress is changed.


```python
def notify(self, args: aspose.words.fields.FieldUpdatingProgressArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [FieldUpdatingProgressArgs](../../fieldupdatingprogressargs/) |  |

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
* class [IFieldUpdatingProgressCallback](../)

