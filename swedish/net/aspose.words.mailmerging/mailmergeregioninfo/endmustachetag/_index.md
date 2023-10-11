---
title: MailMergeRegionInfo.EndMustacheTag
second_title: Aspose.Words för .NET API Referens
description: MailMergeRegionInfo fast egendom. Returnerar en slutmustaschtagg för regionen.
type: docs
weight: 20
url: /sv/net/aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/
---
## MailMergeRegionInfo.EndMustacheTag property

Returnerar en slut-"mustasch"-tagg för regionen.

```csharp
public MustacheTag EndMustacheTag { get; }
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

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* hopsättning [Aspose.Words](../../../)


