---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words for .NET
description: Aspose.Words.MailMerging.MustacheTag class. Represents mustache tag in C#.
type: docs
weight: 4200
url: /net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

Represents "mustache" tag.

```csharp
public class MustacheTag
```

## Properties

| Name | Description |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | Gets the zero-based starting position of the tag from the start of the [`ReferenceRun`](./referencerun/). |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | Gets the run that contains the beginning of the tag. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | Gets the text of the tag. |

## Examples

Shows how to work with the mustache tags.

```csharp
Document document = new Document(MyDir + "Mail merge mustache tags.docx");
document.MailMerge.UseNonMergeFields = true;

MailMergeRegionInfo hierarchy = document.MailMerge.GetRegionsHierarchy();

foreach (MustacheTag mustacheTag in hierarchy.MustacheTags)
{
    Console.WriteLine(mustacheTag.Text);
    Console.WriteLine(mustacheTag.ReferenceOffset);
    Console.WriteLine(mustacheTag.ReferenceRun);
}

foreach (MailMergeRegionInfo region in hierarchy.Regions)
{
    Console.WriteLine(region.StartMustacheTag.Text);
    Console.WriteLine(region.EndMustacheTag.Text);
}
```

### See Also

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../)
