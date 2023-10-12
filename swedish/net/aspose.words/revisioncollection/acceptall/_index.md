---
title: RevisionCollection.AcceptAll
second_title: Aspose.Words för .NET API Referens
description: RevisionCollection metod. Accepterar alla versioner i denna samling.
type: docs
weight: 40
url: /sv/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Accepterar alla versioner i denna samling.

```csharp
public void AcceptAll()
```

### Exempel

Visar hur man jämför dokument.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Att jämföra dokument med revisioner ger ett undantag.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Efter jämförelsen kommer originaldokumentet att få en ny version
// för varje element som är olika i det redigerade dokumentet.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Om du accepterar dessa ändringar förvandlas originaldokumentet till det redigerade dokumentet.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Se även

* class [RevisionCollection](../)
* namnutrymme [Aspose.Words](../../revisioncollection/)
* hopsättning [Aspose.Words](../../../)


