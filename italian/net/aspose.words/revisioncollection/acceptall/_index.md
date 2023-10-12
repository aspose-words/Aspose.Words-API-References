---
title: RevisionCollection.AcceptAll
second_title: Aspose.Words per .NET API Reference
description: RevisionCollection metodo. Accetta tutte le revisioni in questa raccolta.
type: docs
weight: 40
url: /it/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Accetta tutte le revisioni in questa raccolta.

```csharp
public void AcceptAll()
```

### Esempi

Mostra come confrontare i documenti.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Il confronto dei documenti con le revisioni genererà un'eccezione.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Dopo il confronto, il documento originale riceverà una nuova revisione
// per ogni elemento diverso nel documento modificato.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Accettare queste revisioni trasformerà il documento originale nel documento modificato.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Guarda anche

* class [RevisionCollection](../)
* spazio dei nomi [Aspose.Words](../../revisioncollection/)
* assemblea [Aspose.Words](../../../)


