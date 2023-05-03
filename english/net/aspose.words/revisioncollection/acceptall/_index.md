---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
second_title: Aspose.Words for .NET API Reference
description: RevisionCollection AcceptAll method. Accepts all revisions in this collection in C#.
type: docs
weight: 40
url: /net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Accepts all revisions in this collection.

```csharp
public void AcceptAll()
```

## Examples

Shows how to compare documents.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Comparing documents with revisions will throw an exception.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// After the comparison, the original document will gain a new revision
// for every element that is different in the edited document.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Accepting these revisions will transform the original document into the edited document.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### See Also

* class [RevisionCollection](../)
* namespace [Aspose.Words](../../revisioncollection/)
* assembly [Aspose.Words](../../../)
