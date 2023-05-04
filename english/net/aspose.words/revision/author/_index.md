---
title: Revision.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words for .NET
description: Revision Author property. Gets or sets the author of this revision. Can not be empty string or null in C#.
type: docs
weight: 10
url: /net/aspose.words/revision/author/
---
## Revision.Author property

Gets or sets the author of this revision. Can not be empty string or `null`.

```csharp
public string Author { get; set; }
```

## Examples

Shows how to work with revisions in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normal editing of the document does not count as a revision.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// To register our edits as revisions, we need to declare an author, and then start tracking them.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
// The "StartTrackRevisions" method does not affect its value,
// and the document is tracking revisions programmatically despite it having a value of "false".
// If we open this document using Microsoft Word, it will not be tracking revisions.
Assert.IsFalse(doc.TrackRevisions);

// We have added text using the document builder, so the first revision is an insertion-type revision.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Remove a run to create a deletion-type revision.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Adding a new revision places it at the beginning of the revision collection.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Insert revisions show up in the document body even before we accept/reject the revision.
// Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
// also linger in the document until we accept the revision.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Accepting the delete revision will remove its parent node from the paragraph text
// and then remove the collection's revision itself.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Now move the node to create a moving revision type.
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// The moving revision is now at index 1. Reject the revision to discard its contents.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### See Also

* class [Revision](../)
* namespace [Aspose.Words](../../revision/)
* assembly [Aspose.Words](../../../)
