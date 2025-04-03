---
title: Paragraph.isFormatRevision property
linktitle: isFormatRevision property
articleTitle: isFormatRevision property
second_title: Aspose.Words for NodeJs
description: "Paragraph.isFormatRevision property. Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled."
type: docs
weight: 90
url: /nodejs-net/aspose.words/paragraph/isFormatRevision/
---

## Paragraph.isFormatRevision property

Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.


```js
get isFormatRevision(): boolean
```

### Examples

Shows how to check whether a paragraph is a format revision.

```js
let doc = new aw.Document(base.myDir + "Format revision.docx");

// This paragraph is a "Format" revision, which occurs when we change the formatting of existing text
// while tracking revisions in Microsoft Word via "Review" -> "Track changes".
expect(doc.firstSection.body.firstParagraph.isFormatRevision).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

