---
title: Document.startTrackRevisions method
linktitle: startTrackRevisions method
articleTitle: startTrackRevisions method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Document.startTrackRevisions method"
type: docs
weight: 710
url: /nodejs-net/aspose.words/document/startTrackRevisions/
---

## startTrackRevisions(author, dateTime) {#string_date}

Starts automatically marking all further changes you make to the document programmatically as revision changes.


```js
startTrackRevisions(author: string, dateTime: Date)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | string | Initials of the author to use for revisions. |
| dateTime | Date | The date and time to use for revisions. |

### Remarks

If you call this method and then make some changes to the document programmatically,
save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not
recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations
as well as when using [DocumentBuilder](../../documentbuilder/)


This method does not change the [Document.trackRevisions](../trackRevisions/) option and does not use its value
for the purposes of revision tracking.




## startTrackRevisions(author) {#string}

Starts automatically marking all further changes you make to the document programmatically as revision changes.


```js
startTrackRevisions(author: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | string | Initials of the author to use for revisions. |

### Remarks

If you call this method and then make some changes to the document programmatically,
save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not
recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations
as well as when using [DocumentBuilder](../../documentbuilder/)


This method does not change the [Document.trackRevisions](../trackRevisions/) option and does not use its value
for the purposes of revision tracking.




## Examples

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

## See Also

* module [Aspose.Words](../../)
* class [Document](../)
* method [Document.stopTrackRevisions()](../stopTrackRevisions/#default)

