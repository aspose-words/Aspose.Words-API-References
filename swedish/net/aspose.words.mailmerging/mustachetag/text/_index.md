---
title: MustacheTag.Text
second_title: Aspose.Words för .NET API Referens
description: MustacheTag fast egendom. Hämtar taggens text.
type: docs
weight: 30
url: /sv/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Hämtar taggens text.

```csharp
public string Text { get; }
```

### Exempel

Visar hur man arbetar med mustaschtaggarna.

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

### Se även

* class [MustacheTag](../)
* namnutrymme [Aspose.Words.MailMerging](../../mustachetag/)
* hopsättning [Aspose.Words](../../../)


