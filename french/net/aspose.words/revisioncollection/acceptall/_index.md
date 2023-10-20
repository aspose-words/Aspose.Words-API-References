---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: Aspose.Words pour .NET
description: RevisionCollection AcceptAll méthode. Accepte toutes les révisions de cette collection en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Accepte toutes les révisions de cette collection.

```csharp
public void AcceptAll()
```

## Exemples

Montre comment comparer des documents.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// La comparaison de documents avec des révisions lèvera une exception.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Après la comparaison, le document original recevra une nouvelle révision
// pour chaque élément différent dans le document édité.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Accepter ces révisions transformera le document original en document édité.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Voir également

* class [RevisionCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
