---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: Aspose.Words für .NET
description: RevisionCollection AcceptAll methode. Akzeptiert alle Revisionen in dieser Sammlung in C#.
type: docs
weight: 40
url: /de/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Akzeptiert alle Revisionen in dieser Sammlung.

```csharp
public void AcceptAll()
```

## Beispiele

Zeigt, wie Dokumente verglichen werden.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Beim Vergleich von Dokumenten mit Revisionen wird eine Ausnahme ausgelöst.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Nach dem Vergleich erhält das Originaldokument eine neue Revision
// für jedes Element, das im bearbeiteten Dokument anders ist.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Durch das Akzeptieren dieser Überarbeitungen wird das Originaldokument in das bearbeitete Dokument umgewandelt.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Siehe auch

* class [RevisionCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
