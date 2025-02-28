---
title: MailMergeOptions.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words for .NET
description: Optimize your mail merge with the TrimWhitespaces property. Easily manage leading and trailing spaces for cleaner, more professional documents.
type: docs
weight: 110
url: /net/aspose.words.lowcode/mailmergeoptions/trimwhitespaces/
---
## MailMergeOptions.TrimWhitespaces property

Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Remarks

The default value is `true`.

## Examples

Shows how to do mail merge operation for a single record.

```csharp
// There is a several ways to do mail merge operation:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, mailMergeOptions, fieldNames, fieldValues);
```

### See Also

* class [MailMergeOptions](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
