---
title: MustacheTag.ReferenceRun
linktitle: ReferenceRun
articleTitle: ReferenceRun
second_title: Aspose.Words för .NET
description: Upptäck MustacheTag ReferenceRun. Få åtkomst till körningen som markerar starten på din tagg för sömlös datahantering och förbättrad prestanda.
type: docs
weight: 20
url: /sv/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Hämtar körningen som innehåller början av taggen.

```csharp
public Run ReferenceRun { get; }
```

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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
