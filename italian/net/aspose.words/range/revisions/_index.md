---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words per .NET
description: Range Revisions proprietà. Ottiene una raccolta di revisioni modifiche rilevate presenti in questo intervallo in C#.
type: docs
weight: 40
url: /it/net/aspose.words/range/revisions/
---
## Range.Revisions property

Ottiene una raccolta di revisioni (modifiche rilevate) presenti in questo intervallo.

```csharp
public RevisionCollection Revisions { get; }
```

## Osservazioni

La raccolta restituita è una raccolta "attiva", il che significa che se rimuovi parti di un documento che contengono revisioni, le revisioni eliminate scompariranno automaticamente da questa raccolta.

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
