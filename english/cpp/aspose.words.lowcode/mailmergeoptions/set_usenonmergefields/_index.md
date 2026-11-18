---
title: Aspose::Words::LowCode::MailMergeOptions::set_UseNonMergeFields method
linktitle: set_UseNonMergeFields
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::MailMergeOptions::set_UseNonMergeFields method. When true, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags in C++.'
type: docs
weight: 29000
url: /cpp/aspose.words.lowcode/mailmergeoptions/set_usenonmergefields/
---
## MailMergeOptions::set_UseNonMergeFields method


When **true**, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags.

```cpp
void Aspose::Words::LowCode::MailMergeOptions::set_UseNonMergeFields(bool value)
```

## Remarks


Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [UseNonMergeFields](../get_usenonmergefields/) is set to **true**, Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Also, when [UseNonMergeFields](../get_usenonmergefields/) is set to **true**, Aspose.Words will perform mail merge into text tags "{{fieldName}}". These are not fields, but just text tags.
## See Also

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
