---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: Aspose.Words per .NET
description: Scopri il metodo AcceptAll di RevisionCollection per integrare perfettamente tutte le revisioni, migliorando l'efficienza del flusso di lavoro e la collaborazione.
type: docs
weight: 50
url: /it/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Accetta tutte le revisioni in questa raccolta.

```csharp
public void AcceptAll()
```

## Esempi

Mostra come confrontare i documenti.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Il confronto tra documenti e revisioni genererà un'eccezione.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Dopo il confronto, il documento originale otterrà una nuova revisione
// per ogni elemento diverso nel documento modificato.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// L'accettazione di queste revisioni trasformerà il documento originale nel documento modificato.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Guarda anche

* class [RevisionCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
