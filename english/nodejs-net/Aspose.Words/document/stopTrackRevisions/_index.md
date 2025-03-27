---
title: Document.stopTrackRevisions method
linktitle: stopTrackRevisions method
articleTitle: stopTrackRevisions method
second_title: Aspose.Words for NodeJs
description: "Document.stopTrackRevisions method. Stops automatic marking of document changes as revisions."
type: docs
weight: 720
url: /nodejs-net/Aspose.Words/document/stopTrackRevisions/
---

## stopTrackRevisions() {#default}

Stops automatic marking of document changes as revisions.


```js
stopTrackRevisions()
```

### Examples

Shows how to track revisions while editing a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Editing a document usually does not count as a revision until we begin tracking them.
builder.write("Hello world! ");

expect(doc.revisions.count).toEqual(0);
expect(doc.firstSection.body.paragraphs.at(0).runs.at(0).isInsertRevision).toEqual(false);

doc.startTrackRevisions("John Doe");

builder.write("Hello again! ");

expect(doc.revisions.count).toEqual(1);
expect(doc.firstSection.body.paragraphs.at(0).runs.at(1).isInsertRevision).toEqual(true);
expect(doc.revisions.at(0).author).toEqual("John Doe");
expect((Date.now() - doc.revisions.at(0).dateTime).Milliseconds <= 10).toEqual(true);

// Stop tracking revisions to not count any future edits as revisions.
doc.stopTrackRevisions();
builder.write("Hello again! ");

expect(doc.revisions.count).toEqual(1);
expect(doc.firstSection.body.paragraphs.at(0).runs.at(2).isInsertRevision).toEqual(false);

// Creating revisions gives them a date and time of the operation.
// We can disable this by passing DateTime.minValue when we start tracking revisions.
doc.startTrackRevisions("John Doe", DateTime.minValue);
builder.write("Hello again! ");

expect(doc.revisions.count).toEqual(2);
expect(doc.revisions.at(1).author).toEqual("John Doe");
expect(doc.revisions.at(1).dateTime).toEqual(DateTime.minValue);

// We can accept/reject these revisions programmatically
// by calling methods such as aw.Document.acceptAllRevisions, or each revision's Accept method.
// In Microsoft Word, we can process them manually via "Review" -> "Changes".
doc.save(base.artifactsDir + "Document.startTrackRevisions.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)
* method [Document.startTrackRevisions()](../startTrackRevisions/#string_date)

