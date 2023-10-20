---
title: MailMergeRegionInfo.StartMustacheTag
linktitle: StartMustacheTag
articleTitle: StartMustacheTag
second_title: Aspose.Words för .NET
description: MailMergeRegionInfo StartMustacheTag fast egendom. Returnerar en start mustaschtagg för regionen i C#.
type: docs
weight: 100
url: /sv/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

Returnerar en start "mustasch"-tagg för regionen.

```csharp
public MustacheTag StartMustacheTag { get; }
```

## Exempel

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
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
