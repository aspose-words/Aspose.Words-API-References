---
title: Aspose::Words::LowCode::MailMerging::MailMergeOptions::get_UseNonMergeFields method
linktitle: get_UseNonMergeFields
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::MailMerging::MailMergeOptions::get_UseNonMergeFields method. When true, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.lowcode.mailmerging/mailmergeoptions/get_usenonmergefields/
---
## MailMergeOptions::get_UseNonMergeFields method


When **true**, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags.

```cpp
bool Aspose::Words::LowCode::MailMerging::MailMergeOptions::get_UseNonMergeFields() const
```

## Remarks


Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When [UseNonMergeFields](./) is set to **true**, Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Also, when [UseNonMergeFields](./) is set to **true**, Aspose.Words will perform mail merge into text tags "{{fieldName}}". These are not fields, but just text tags. 
## See Also

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
