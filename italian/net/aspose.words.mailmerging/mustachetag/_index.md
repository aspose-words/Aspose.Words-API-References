---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.MailMerging.MustacheTag: gestisci in modo efficiente i tag mustache per un'automazione fluida dei documenti e una fusione di posta migliorata.
type: docs
weight: 4570
url: /it/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

Rappresenta il tag "baffi".

```csharp
public class MustacheTag
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | Ottiene la posizione iniziale basata su zero del tag dall'inizio del[`ReferenceRun`](./referencerun/) . |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | Ottiene l'esecuzione che contiene l'inizio del tag. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | Ottiene il testo del tag. |

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

* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)
