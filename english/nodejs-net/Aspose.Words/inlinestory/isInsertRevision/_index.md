---
title: InlineStory.isInsertRevision property
linktitle: isInsertRevision property
articleTitle: isInsertRevision property
second_title: Aspose.Words for NodeJs
description: "InlineStory.isInsertRevision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 40
url: /nodejs-net/aspose.words/inlinestory/isInsertRevision/
---

## InlineStory.isInsertRevision property

Returns true if this object was inserted in Microsoft Word while change tracking was enabled.


```js
get isInsertRevision(): boolean
```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```js
let doc = new aw.Document(base.myDir + "Revision footnotes.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to undo and discard the proposed change.
expect(doc.hasRevisions).toEqual(true);

var footnotes = doc.getChildNodes(aw.NodeType.Footnote, true);

expect(footnotes.count).toEqual(5);

// Below are five types of revisions that can flag an InlineStory node.
// 1 -  An "insert" revision:
// This revision occurs when we insert text while tracking changes.
expect(footnotes.at(2).asFootnote().isInsertRevision).toEqual(true);

// 2 -  A "move from" revision:
// When we highlight text in Microsoft Word, and then drag it to a different place in the document
// while tracking changes, two revisions appear.
// The "move from" revision is a copy of the text originally before we moved it.
expect(footnotes.at(4).asFootnote().isMoveFromRevision).toEqual(true);

// 3 -  A "move to" revision:
// The "move to" revision is the text that we moved in its new position in the document.
// "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
// Accepting a move revision deletes the "move from" revision and its text,
// and keeps the text from the "move to" revision.
// Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
expect(footnotes.at(1).asFootnote().isMoveToRevision).toEqual(true);

// 4 -  A "delete" revision:
// This revision occurs when we delete text while tracking changes. When we delete text like this,
// it will stay in the document as a revision until we either accept the revision,
// which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
expect(footnotes.at(3).asFootnote().isDeleteRevision).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [InlineStory](../)

