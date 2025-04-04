---
title: Revision.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Node.js
description: "Revision.accept method. Accepts this revision."
type: docs
weight: 70
url: /nodejs-net/aspose.words/revision/accept/
---

## accept() {#default}

Accepts this revision.


```js
accept()
```

### Examples

Shows how to work with revisions in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Normal editing of the document does not count as a revision.
builder.write("This does not count as a revision. ");

expect(doc.hasRevisions).toEqual(false);

// To register our edits as revisions, we need to declare an author, and then start tracking them.
doc.startTrackRevisions("John Doe", Date.now());

builder.write("This is revision #1. ");

expect(doc.hasRevisions).toEqual(true);
expect(doc.revisions.count).toEqual(1);

// This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
// The "StartTrackRevisions" method does not affect its value,
// and the document is tracking revisions programmatically despite it having a value of "false".
// If we open this document using Microsoft Word, it will not be tracking revisions.
expect(doc.trackRevisions).toEqual(false);

// We have added text using the document builder, so the first revision is an insertion-type revision.
let revision = doc.revisions.at(0);
expect(revision.author).toEqual("John Doe");
expect(revision.parentNode.getText()).toEqual("This is revision #1. ");
expect(revision.revisionType).toEqual(aw.RevisionType.Insertion);
expect(Date.now().Date).toEqual(revision.dateTime.date);
expect(revision.group).toEqual(doc.revisions.groups.at(0));

// Remove a run to create a deletion-type revision.
doc.firstSection.body.firstParagraph.runs.at(0).remove();

// Adding a new revision places it at the beginning of the revision collection.
expect(doc.revisions.at(0).revisionType).toEqual(aw.RevisionType.Deletion);
expect(doc.revisions.count).toEqual(2);

// Insert revisions show up in the document body even before we accept/reject the revision.
// Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
// also linger in the document until we accept the revision.
expect(doc.getText().trim()).toEqual("This does not count as a revision. This is revision #1.");

// Accepting the delete revision will remove its parent node from the paragraph text
// and then remove the collection's revision itself.
doc.revisions.at(0).accept();

expect(doc.revisions.count).toEqual(1);
expect(doc.getText().trim()).toEqual("This is revision #1.");

builder.writeln("");
builder.write("This is revision #2.");

// Now move the node to create a moving revision type.
let node = doc.firstSection.body.paragraphs.at(1);
let endNode = doc.firstSection.body.paragraphs.at(1).nextSibling;
let referenceNode = doc.firstSection.body.paragraphs.at(0);

while (node != endNode)
{
  let nextNode = node.nextSibling;
  doc.firstSection.body.insertBefore(node, referenceNode);
  node = nextNode;
}

expect(doc.revisions.at(0).revisionType).toEqual(aw.RevisionType.Moving);
expect(doc.revisions.count).toEqual(8);
expect(doc.getText().trim()).toEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.");

// The moving revision is now at index 1. Reject the revision to discard its contents.
doc.revisions.at(1).reject();

expect(doc.revisions.count).toEqual(6);
expect(doc.getText().trim()).toEqual("This is revision #1. \rThis is revision #2.");
```

### See Also

* module [Aspose.Words](../../)
* class [Revision](../)

