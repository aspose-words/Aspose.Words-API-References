---
title: FieldMergingArgs.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldMergingArgs.text property. Gets or sets the text that will be inserted into the document for the current merge field."
type: docs
weight: 10
url: /python-net/aspose.words.mailmerging/fieldmergingargs/text/
---

## FieldMergingArgs.text property

Gets or sets the text that will be inserted into the document for the current merge field.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Remarks

When your event handler is called, this property is set to ``None``.

If you leave Text as ``None``, the mail merge engine will insert [FieldMergingArgsBase.field_value](../../fieldmergingargsbase/field_value/) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field.




### See Also

* module [aspose.words.mailmerging](../../)
* class [FieldMergingArgs](../)

