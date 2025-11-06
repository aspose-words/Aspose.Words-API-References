---
title: Revision Class
linktitle: Revision
articleTitle: Revision
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words.Revision class to manage tracked changes in documents. Easily identify revision types for seamless document editing.
type: docs
weight: 5540
url: /net/aspose.words/revision/
---
## Revision class

Represents a revision (tracked change) in a document node or style. Use [`RevisionType`](./revisiontype/) to check the type of this revision.

To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/net/track-changes-in-a-document/) documentation article.

```csharp
public class Revision
```

## Properties

| Name | Description |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | Gets or sets the author of this revision. Can not be empty string or `null`. |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | Gets or sets the date/time of this revision. |
| [Group](../../aspose.words/revision/group/) { get; } | Gets the revision group. Returns `null` if the revision does not belong to any group. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | Gets the immediate parent node (owner) of this revision. This property will work for any revision type other than StyleDefinitionChange. |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | Gets the immediate parent style (owner) of this revision. This property will work for only for the StyleDefinitionChange revision type. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | Gets the type of this revision. |

## Methods

| Name | Description |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | Accepts this revision. |
| [Reject](../../aspose.words/revision/reject/)() | Reject this revision. |

## Examples

Shows how to work with revisions in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normal editing of the document does not count as a revision.
builder.Write("This does not count as a revision. ");

Assert.That(doc.HasRevisions, Is.False);

// To register our edits as revisions, we need to declare an author, and then start tracking them.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.That(doc.HasRevisions, Is.True);
Assert.That(doc.Revisions.Count, Is.EqualTo(1));

// This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
// The "StartTrackRevisions" method does not affect its value,
// and the document is tracking revisions programmatically despite it having a value of "false".
// If we open this document using Microsoft Word, it will not be tracking revisions.
Assert.That(doc.TrackRevisions, Is.False);

// We have added text using the document builder, so the first revision is an insertion-type revision.
Revision revision = doc.Revisions[0];
Assert.That(revision.Author, Is.EqualTo("John Doe"));
Assert.That(revision.ParentNode.GetText(), Is.EqualTo("This is revision #1. "));
Assert.That(revision.RevisionType, Is.EqualTo(RevisionType.Insertion));
Assert.That(DateTime.Now.Date, Is.EqualTo(revision.DateTime.Date));
Assert.That(revision.Group, Is.EqualTo(doc.Revisions.Groups[0]));

// Remove a run to create a deletion-type revision.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Adding a new revision places it at the beginning of the revision collection.
Assert.That(doc.Revisions[0].RevisionType, Is.EqualTo(RevisionType.Deletion));
Assert.That(doc.Revisions.Count, Is.EqualTo(2));

// Insert revisions show up in the document body even before we accept/reject the revision.
// Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
// also linger in the document until we accept the revision.
Assert.That(doc.GetText().Trim(), Is.EqualTo("This does not count as a revision. This is revision #1."));

// Accepting the delete revision will remove its parent node from the paragraph text
// and then remove the collection's revision itself.
doc.Revisions[0].Accept();

Assert.That(doc.Revisions.Count, Is.EqualTo(1));
Assert.That(doc.GetText().Trim(), Is.EqualTo("This is revision #1."));

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

Assert.That(doc.Revisions[0].RevisionType, Is.EqualTo(RevisionType.Moving));
Assert.That(doc.Revisions.Count, Is.EqualTo(8));
Assert.That(doc.GetText().Trim(), Is.EqualTo("This is revision #2.\rThis is revision #1. \rThis is revision #2."));

// The moving revision is now at index 1. Reject the revision to discard its contents.
doc.Revisions[1].Reject();

Assert.That(doc.Revisions.Count, Is.EqualTo(6));
Assert.That(doc.GetText().Trim(), Is.EqualTo("This is revision #1. \rThis is revision #2."));
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
