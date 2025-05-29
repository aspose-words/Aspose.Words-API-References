---
title: MustacheTag.ReferenceRun
linktitle: ReferenceRun
articleTitle: ReferenceRun
second_title: Aspose.Words per .NET
description: Scopri MustacheTag ReferenceRun. Accedi all'esecuzione che segna l'inizio del tuo tag per una gestione dei dati fluida e prestazioni migliorate.
type: docs
weight: 20
url: /it/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Ottiene l'esecuzione che contiene l'inizio del tag.

```csharp
public Run ReferenceRun { get; }
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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
