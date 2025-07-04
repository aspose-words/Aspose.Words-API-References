---
title: InlineStory.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words for .NET
description: Discover how InlineStory's IsDeleteRevision property enhances your Microsoft Word experience by tracking deleted changes effortlessly.
type: docs
weight: 30
url: /net/aspose.words/inlinestory/isdeleterevision/
---
## InlineStory.IsDeleteRevision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

```csharp
public bool IsDeleteRevision { get; }
```

## Examples

Shows how to view revision-related properties of InlineStory nodes.

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.Words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to undo and discard the proposed change.
Assert.That(doc.HasRevisions, Is.True);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.That(footnotes.Count, Is.EqualTo(5));

// Below are five types of revisions that can flag an InlineStory node.
// 1 -  An "insert" revision:
// This revision occurs when we insert text while tracking changes.
Assert.That(footnotes[2].IsInsertRevision, Is.True);

// 2 -  A "move from" revision:
// When we highlight text in Microsoft Word, and then drag it to a different place in the document
// while tracking changes, two revisions appear.
// The "move from" revision is a copy of the text originally before we moved it.
Assert.That(footnotes[4].IsMoveFromRevision, Is.True);

// 3 -  A "move to" revision:
// The "move to" revision is the text that we moved in its new position in the document.
// "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
// Accepting a move revision deletes the "move from" revision and its text,
// and keeps the text from the "move to" revision.
// Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
Assert.That(footnotes[1].IsMoveToRevision, Is.True);

// 4 -  A "delete" revision:
// This revision occurs when we delete text while tracking changes. When we delete text like this,
// it will stay in the document as a revision until we either accept the revision,
// which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
Assert.That(footnotes[3].IsDeleteRevision, Is.True);
```

### See Also

* class [InlineStory](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
