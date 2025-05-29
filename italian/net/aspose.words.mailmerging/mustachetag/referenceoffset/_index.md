---
title: MustacheTag.ReferenceOffset
linktitle: ReferenceOffset
articleTitle: ReferenceOffset
second_title: Aspose.Words per .NET
description: Scopri la proprietà MustacheTag ReferenceOffset, che rivela la posizione iniziale basata su zero dei tag nel tuo ReferenceRun per una gestione precisa dei dati.
type: docs
weight: 10
url: /it/net/aspose.words.mailmerging/mustachetag/referenceoffset/
---
## MustacheTag.ReferenceOffset property

Ottiene la posizione iniziale basata su zero del tag dall'inizio del[`ReferenceRun`](../referencerun/) .

```csharp
public int ReferenceOffset { get; }
```

## Esempi

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
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
