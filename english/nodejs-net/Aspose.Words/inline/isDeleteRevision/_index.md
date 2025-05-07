---
title: Inline.isDeleteRevision property
linktitle: isDeleteRevision property
articleTitle: isDeleteRevision property
second_title: Aspose.Words for Node.js
description: "Inline.isDeleteRevision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 20
url: /nodejs-net/aspose.words/inline/isDeleteRevision/
---

## Inline.isDeleteRevision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.


```js
get isDeleteRevision(): boolean
```

### Examples

Shows how to determine the revision type of an inline node.

```js
let doc = new aw.Document(base.myDir + "Revision runs.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to change the proposed change effectively.
expect(doc.revisions.count).toEqual(6);

// The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
let run = doc.revisions.at(0).parentNode.asRun();

let firstParagraph = run.parentParagraph;
let runs = firstParagraph.runs.toArray();

expect(runs.length).toEqual(6);

// Below are five types of revisions that can flag an Inline node.
// 1 -  An "insert" revision:
// This revision occurs when we insert text while tracking changes.
expect(runs.at(2).isInsertRevision).toEqual(true);

// 2 -  A "format" revision:
// This revision occurs when we change the formatting of text while tracking changes.
expect(runs.at(2).isFormatRevision).toEqual(true);

// 3 -  A "move from" revision:
// When we highlight text in Microsoft Word, and then drag it to a different place in the document
// while tracking changes, two revisions appear.
// The "move from" revision is a copy of the text originally before we moved it.
expect(runs.at(4).isMoveFromRevision).toEqual(true);

// 4 -  A "move to" revision:
// The "move to" revision is the text that we moved in its new position in the document.
// "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
// Accepting a move revision deletes the "move from" revision and its text,
// and keeps the text from the "move to" revision.
// Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
expect(runs.at(1).isMoveToRevision).toEqual(true);

// 5 -  A "delete" revision:
// This revision occurs when we delete text while tracking changes. When we delete text like this,
// it will stay in the document as a revision until we either accept the revision,
// which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
expect(runs.at(5).isDeleteRevision).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [Inline](../)

