---
title: ReportBuilderOptions.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words for .NET
description: Discover the ReportBuilderOptions MissingMemberMessage property. Easily customize messages for missing object references, enhancing user experience effortlessly.
type: docs
weight: 30
url: /net/aspose.words.lowcode/reportbuilderoptions/missingmembermessage/
---
## ReportBuilderOptions.MissingMemberMessage property

Gets or sets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. The default value is an empty string.

```csharp
public string MissingMemberMessage { get; set; }
```

## Remarks

The property should be used in conjunction with the AllowMissingMembers option. Otherwise, an exception is thrown when a missing member of an object is encountered.

The property affects only printing of a template expression representing a plain reference to a missing object member. For example, printing of a binary operator, one of which operands references a missing object member, is not affected.

The value of this property cannot be set to null.

### See Also

* class [ReportBuilderOptions](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
