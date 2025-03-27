---
title: Paragraph.isMoveToRevision property
linktitle: isMoveToRevision property
articleTitle: isMoveToRevision property
second_title: Aspose.Words for NodeJs
description: "Paragraph.isMoveToRevision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 140
url: /nodejs-net/Aspose.Words/paragraph/isMoveToRevision/
---

## Paragraph.isMoveToRevision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```js
get isMoveToRevision(): boolean
```

### Examples

Shows how to check whether a paragraph is a move revision.

```js
let doc = new aw.Document(base.myDir + "Revisions.docx");

// This document contains "Move" revisions, which appear when we highlight text with the cursor,
// and then drag it to move it to another location
// while tracking revisions in Microsoft Word via "Review" -> "Track changes".
expect(Array.from(doc.revisions).filter(r => r.revisionType == aw.RevisionType.Moving).length).toEqual(6);

let paragraphs = doc.firstSection.body.paragraphs;

// Move revisions consist of pairs of "Move from", and "Move to" revisions. 
// These revisions are potential changes to the document that we can either accept or reject.
// Before we accept/reject a move revision, the document
// must keep track of both the departure and arrival destinations of the text.
// The second and the fourth paragraph define one such revision, and thus both have the same contents.
expect(paragraphs.at(3).getText()).toEqual(paragraphs.at(1).getText());

// The "Move from" revision is the paragraph where we dragged the text from.
// If we accept the revision, this paragraph will disappear,
// and the other will remain and no longer be a revision.
expect(paragraphs.at(1).isMoveFromRevision).toEqual(true);

// The "Move to" revision is the paragraph where we dragged the text to.
// If we reject the revision, this paragraph instead will disappear, and the other will remain.
expect(paragraphs.at(3).isMoveToRevision).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

