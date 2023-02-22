---
title: RevisionCollection.AcceptAll
second_title: Aspose.Words für .NET-API-Referenz
description: RevisionCollection methode. Akzeptiert alle Überarbeitungen in dieser Sammlung.
type: docs
weight: 40
url: /de/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Akzeptiert alle Überarbeitungen in dieser Sammlung.

```csharp
public void AcceptAll()
```

### Beispiele

Zeigt, wie Dokumente verglichen werden.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Der Vergleich von Dokumenten mit Revisionen löst eine Ausnahme aus.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Nach dem Vergleich erhält das Originaldokument eine neue Revision
// für jedes Element, das im bearbeiteten Dokument anders ist.
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Wenn Sie diese Überarbeitungen akzeptieren, wird das Originaldokument in das bearbeitete Dokument umgewandelt.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Siehe auch

* class [RevisionCollection](../)
* namensraum [Aspose.Words](../../revisioncollection/)
* Montage [Aspose.Words](../../../)


