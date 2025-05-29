---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.MailMerging.MustacheTag – hanterar effektivt mustaschtaggar för sömlös dokumentautomation och förbättrad sammanslagning av e-post.
type: docs
weight: 4570
url: /sv/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

Representerar taggen "mustasch".

```csharp
public class MustacheTag
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | Hämtar den nollbaserade startpositionen för taggen från början av[`ReferenceRun`](./referencerun/) . |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | Hämtar körningen som innehåller början av taggen. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | Hämtar taggens text. |

## Exempel

Visar hur man arbetar med mustaschtaggar.

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

* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)
