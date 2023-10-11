---
title: MailMergeRegionInfo.StartMustacheTag
second_title: Aspose.Words per .NET API Reference
description: MailMergeRegionInfo proprietà. Restituisce un tag iniziale baffi per la regione.
type: docs
weight: 100
url: /it/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

Restituisce un tag iniziale "baffi" per la regione.

```csharp
public MustacheTag StartMustacheTag { get; }
```

### Esempi

Mostra come lavorare con le etichette dei baffi.

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

### Guarda anche

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* assemblea [Aspose.Words](../../../)


