---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words for .NET
description: Streamline your editing process with the AcceptAllRevisions method, effortlessly accepting all tracked changes in your document for a polished final version.
type: docs
weight: 540
url: /net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Accepts all tracked changes in the document.

```csharp
public void AcceptAllRevisions()
```

## Remarks

This method is a shortcut for [`AcceptAll`](../../revisioncollection/acceptall/).

## Examples

Shows how to accept all tracking changes in the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Edit the document while tracking changes to create a few revisions.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! ");
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.That(doc.Revisions.Count, Is.EqualTo(3));

// We can iterate through every revision and accept/reject it as a part of our document.
// If we know we wish to accept every revision, we can do it more straightforwardly so by calling this method.
doc.AcceptAllRevisions();

Assert.That(doc.Revisions.Count, Is.EqualTo(0));
Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello world! Hello again! This is another revision."));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
