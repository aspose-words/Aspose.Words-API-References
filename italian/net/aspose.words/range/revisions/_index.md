---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words per .NET
description: Scopri le revisioni di Range. Monitora e gestisci le modifiche agli immobili senza sforzo grazie alla nostra completa raccolta di revisioni per una maggiore chiarezza del progetto.
type: docs
weight: 40
url: /it/net/aspose.words/range/revisions/
---
## Range.Revisions property

Ottiene una raccolta di revisioni (modifiche tracciate) presenti in questo intervallo.

```csharp
public RevisionCollection Revisions { get; }
```

## Osservazioni

La raccolta restituita è una raccolta "live", il che significa che se si rimuovono parti di un documento che contengono revisioni, le revisioni eliminate scompariranno automaticamente da questa raccolta.

## Esempi

Mostra come lavorare con le revisioni nell'intervallo.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Rifiuta le revisioni della prima sezione.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Guarda anche

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
