---
title: MailMerge.use_non_merge_fields property
linktitle: use_non_merge_fields property
articleTitle: use_non_merge_fields property
second_title: Aspose.Words for Python
description: "MailMerge.use_non_merge_fields property. When ``True``, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into {{fieldName}} tags."
type: docs
weight: 150
url: /python-net/aspose.words.mailmerging/mailmerge/use_non_merge_fields/
---

## MailMerge.use_non_merge_fields property

When ``True``, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and
also into "{{fieldName}}" tags.



```python
@property
def use_non_merge_fields(self) -> bool:
    ...

@use_non_merge_fields.setter
def use_non_merge_fields(self, value: bool):
    ...

```

### Remarks

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting
built using other fields and had many documents created this way. To simplify migration (and because this
approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [MailMerge.use_non_merge_fields](./) is set to ``True``, Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Also, when [MailMerge.use_non_merge_fields](./) is set to ``True``, Aspose.Words will perform mail merge into text tags
"{{fieldName}}". These are not fields, but just text tags.




### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

