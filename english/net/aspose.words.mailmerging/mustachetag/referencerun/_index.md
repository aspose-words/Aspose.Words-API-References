---
title: MustacheTag.ReferenceRun
linktitle: ReferenceRun
articleTitle: ReferenceRun
second_title: Aspose.Words for .NET
description: Discover MustacheTag ReferenceRun, Access the run that marks the start of your tag for seamless data management and enhanced performance.
type: docs
weight: 20
url: /net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Gets the run that contains the beginning of the tag.

```csharp
public Run ReferenceRun { get; }
```

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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
