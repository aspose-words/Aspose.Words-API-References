---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.RevisionGroup, progettata per gestire e organizzare in modo efficiente gli oggetti Revision sequenziali per una modifica semplificata dei documenti.
type: docs
weight: 5520
url: /it/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Rappresenta un gruppo di elementi sequenziali[`Revision`](../revision/) oggetti.

Per saperne di più, visita il[Traccia le modifiche in un documento](https://docs.aspose.com/words/net/track-changes-in-a-document/) articolo di documentazione.

```csharp
public class RevisionGroup
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Ottiene l'autore di questo gruppo di revisione. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Ottiene il tipo di revisioni incluse in questo gruppo. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Restituisce il testo inserito/eliminato/spostato o la descrizione della modifica del formato. |

## Esempi

Mostra come stampare informazioni su un gruppo di revisioni in un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
