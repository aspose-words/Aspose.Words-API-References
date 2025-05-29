---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: Aspose.Words för .NET
description: Upptäck RevisionCollection AcceptAll-metoden för att sömlöst integrera alla revisioner, vilket förbättrar effektiviteten i ditt arbetsflöde och samarbetet.
type: docs
weight: 50
url: /sv/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Accepterar alla revisioner i den här samlingen.

```csharp
public void AcceptAll()
```

## Exempel

Visar hur man jämför dokument.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Jämförelse av dokument med revisioner kommer att utlösa ett undantag.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// Efter jämförelsen kommer originaldokumentet att få en ny revision
// för varje element som är annorlunda i det redigerade dokumentet.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Om du accepterar dessa ändringar omvandlas originaldokumentet till det redigerade dokumentet.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Se även

* class [RevisionCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
