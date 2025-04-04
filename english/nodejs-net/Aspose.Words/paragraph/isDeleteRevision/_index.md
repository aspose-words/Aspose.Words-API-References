---
title: Paragraph.isDeleteRevision property
linktitle: isDeleteRevision property
articleTitle: isDeleteRevision property
second_title: Aspose.Words for Node.js
description: "Paragraph.isDeleteRevision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 40
url: /nodejs-net/aspose.words/paragraph/isDeleteRevision/
---

## Paragraph.isDeleteRevision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.


```js
get isDeleteRevision(): boolean
```

### Examples

Shows how to work with revision paragraphs.

```js
let doc = new aw.Document();
let body = doc.firstSection.body;
let para = body.firstParagraph;

para.appendChild(new aw.Run(doc, "Paragraph 1. "));
body.appendParagraph("Paragraph 2. ");
body.appendParagraph("Paragraph 3. ");

// The above paragraphs are not revisions.
// Paragraphs that we add after starting revision tracking will register as "Insert" revisions.
doc.startTrackRevisions("John Doe", Date.now());

para = body.appendParagraph("Paragraph 4. ");

expect(para.isInsertRevision).toEqual(true);

// Paragraphs that we remove after starting revision tracking will register as "Delete" revisions.
let paragraphs = body.paragraphs;

expect(paragraphs.count).toEqual(4);

para = paragraphs.at(2);
para.remove();

// Such paragraphs will remain until we either accept or reject the delete revision.
// Accepting the revision will remove the paragraph for good,
// and rejecting the revision will leave it in the document as if we never deleted it.
expect(paragraphs.count).toEqual(4);
expect(para.isDeleteRevision).toEqual(true);

// Accept the revision, and then verify that the paragraph is gone.
doc.acceptAllRevisions();

expect(paragraphs.count).toEqual(3);
expect(para.count).toEqual(0);
expect("Paragraph 1. \rParagraph 2. \rParagraph 4.").toEqual(doc.getText().trim());
```

### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

