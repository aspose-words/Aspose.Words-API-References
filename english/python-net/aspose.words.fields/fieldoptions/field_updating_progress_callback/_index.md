---
title: FieldOptions.field_updating_progress_callback property
linktitle: field_updating_progress_callback property
articleTitle: field_updating_progress_callback property
second_title: Aspose.Words for Python
description: "FieldOptions.field_updating_progress_callback property. Gets or sets [IFieldUpdatingProgressCallback](../../ifieldupdatingprogresscallback/) implementation."
type: docs
weight: 130
url: /python-net/aspose.words.fields/fieldoptions/field_updating_progress_callback/
---

## FieldOptions.field_updating_progress_callback property

Gets or sets [IFieldUpdatingProgressCallback](../../ifieldupdatingprogresscallback/) implementation.



```python
@property
def field_updating_progress_callback(self) -> aspose.words.fields.IFieldUpdatingProgressCallback:
    ...

@field_updating_progress_callback.setter
def field_updating_progress_callback(self, value: aspose.words.fields.IFieldUpdatingProgressCallback):
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
* class [FieldOptions](../)

