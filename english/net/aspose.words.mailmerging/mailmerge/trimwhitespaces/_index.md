---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words for .NET
description: Optimize your mail merge process with the TrimWhitespaces property, ensuring clean data by removing leading and trailing spaces for accurate results.
type: docs
weight: 130
url: /net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Gets or sets a value indicating whether trailing and leading whitespaces are trimmed from mail merge values.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Remarks

The default value is `true`.

## Examples

Shows how to trim whitespaces from values of a data source while executing a mail merge.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.That(doc.GetText(), Is.EqualTo(trimWhitespaces ? "hello world!\f" : "\t hello world! \f"));
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
