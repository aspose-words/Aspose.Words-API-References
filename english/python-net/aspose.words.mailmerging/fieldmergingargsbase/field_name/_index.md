---
title: FieldMergingArgsBase.field_name property
linktitle: field_name property
articleTitle: field_name property
second_title: Aspose.Words for Python
description: "FieldMergingArgsBase.field_name property. Gets the name of the merge field in the data source."
type: docs
weight: 40
url: /python-net/aspose.words.mailmerging/fieldmergingargsbase/field_name/
---

## FieldMergingArgsBase.field_name property

Gets the name of the merge field in the data source.


```python
@property
def field_name(self) -> str:
    ...

```

### Remarks

If you have a mapping from a document field name to a different data source field name,
then this is the mapped field name.

If you specified a field name prefix, for example "Image:MyFieldName" in the document,
then [FieldMergingArgsBase.field_name](./) returns field name without the prefix, that is "MyFieldName".




### See Also

* module [aspose.words.mailmerging](../../)
* class [FieldMergingArgsBase](../)

