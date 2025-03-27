---
title: Range.revisions property
linktitle: revisions property
articleTitle: revisions property
second_title: Aspose.Words for NodeJs
description: "Range.revisions property. Gets a collection of revisions (tracked changes) that exist in this range."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/range/revisions/
---

## Range.revisions property

Gets a collection of revisions (tracked changes) that exist in this range.


```js
get revisions(): Aspose.Words.RevisionCollection
```

### Remarks

The returned collection is a "live" collection, which means if you remove parts of a document that contain
revisions, the deleted revisions will automatically disappear from this collection.




### Examples

Shows how to work with revisions in range.

```js
let doc = new aw.Document(base.myDir + "Revisions.docx");

let paragraph = doc.firstSection.body.firstParagraph;
for (let revision of paragraph.range.revisions)
{
  if (revision.revisionType == aw.RevisionType.Deletion)
    revision.accept();
}

// Reject the first section revisions.
doc.firstSection.range.revisions.rejectAll();
```

### See Also

* module [Aspose.Words](../../)
* class [Range](../)

