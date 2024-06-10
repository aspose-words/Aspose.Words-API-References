---
title: FieldMergingArgsBase.document_field_name property
linktitle: document_field_name property
articleTitle: document_field_name property
second_title: Aspose.Words for Python
description: "FieldMergingArgsBase.document_field_name property. Gets the name of the merge field as specified in the document."
type: docs
weight: 20
url: /python-net/aspose.words.mailmerging/fieldmergingargsbase/document_field_name/
---

## FieldMergingArgsBase.document_field_name property

Gets the name of the merge field as specified in the document.


```python
@property
def document_field_name(self) -> str:
    ...

```

### Remarks

If you have a mapping from a document field name to a different data source field name,
then this is the original field name as specified in the document.

If you specified a field name prefix, for example "Image:MyFieldName" in the document,
then [FieldMergingArgsBase.document_field_name](./) returns field name without the prefix, that is "MyFieldName".




### See Also

* module [aspose.words.mailmerging](../../)
* class [FieldMergingArgsBase](../)

