---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words for .NET
description: Unlock advanced mail merge capabilities with the UseNonMergeFields property. Seamlessly integrate MERGEFIELD and other field types for enhanced document customization.
type: docs
weight: 130
url: /net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

When `true`, specifies that in addition to MERGEFIELD fields, mail merge is performed into some other types of fields and also into "{{fieldName}}" tags.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Remarks

Normally, mail merge is only performed into MERGEFIELD fields, but several customers had their reporting built using other fields and had many documents created this way. To simplify migration (and because this approach was independently used by several customers) the ability to mail merge into other fields was introduced.

When `UseNonMergeFields` is set to `true`, Aspose.Words will perform mail merge into the following fields:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

Also, when `UseNonMergeFields` is set to `true`, Aspose.Words will perform mail merge into text tags "{{fieldName}}". These are not fields, but just text tags.

### See Also

* class [MailMergeOptions](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
