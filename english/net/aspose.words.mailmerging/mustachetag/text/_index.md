---
title: MustacheTag.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: Discover the MustacheTag Text property to effortlessly retrieve and utilize tag text for enhanced data handling and seamless integration.
type: docs
weight: 30
url: /net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Gets the text of the tag.

```csharp
public string Text { get; }
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

* class [MustacheTag](../)
* namespace [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assembly [Aspose.Words](../../../)
