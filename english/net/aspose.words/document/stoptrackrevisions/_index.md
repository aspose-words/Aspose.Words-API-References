---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words for .NET
description: Learn how to use the StopTrackRevisions method to prevent automatic document change markings, enhancing your editing efficiency and document clarity.
type: docs
weight: 770
url: /net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Stops automatic marking of document changes as revisions.

```csharp
public void StopTrackRevisions()
```

## Examples

Shows how to track revisions while editing a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Editing a document usually does not count as a revision until we begin tracking them.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Stop tracking revisions to not count any future edits as revisions.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Creating revisions gives them a date and time of the operation.
// We can disable this by passing DateTime.MinValue when we start tracking revisions.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// We can accept/reject these revisions programmatically
// by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
// In Microsoft Word, we can process them manually via "Review" -> "Changes".
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### See Also

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
