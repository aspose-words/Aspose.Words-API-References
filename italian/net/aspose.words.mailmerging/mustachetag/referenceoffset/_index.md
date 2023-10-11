---
title: MustacheTag.ReferenceOffset
second_title: Aspose.Words per .NET API Reference
description: MustacheTag proprietà. Ottiene la posizione iniziale in base zero del tag dallinizio del fileReferenceRun .
type: docs
weight: 10
url: /it/net/aspose.words.mailmerging/mustachetag/referenceoffset/
---
## MustacheTag.ReferenceOffset property

Ottiene la posizione iniziale in base zero del tag dall'inizio del file[`ReferenceRun`](../referencerun/) .

```csharp
public int ReferenceOffset { get; }
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

* class [MustacheTag](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../mustachetag/)
* assemblea [Aspose.Words](../../../)


