---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words for .NET
description: Discover the MailMerge RestartListsAtEachSection property—control list resets in each section for seamless mail merges. Enhance your document precision today!
type: docs
weight: 110
url: /net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Gets or sets a value indicating whether lists are restarted at each section after executing of a mail merge.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Remarks

The default value is `true`.

## Examples

Shows how to control whether or not list numbering is restarted at each section when mail merge is performed.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
