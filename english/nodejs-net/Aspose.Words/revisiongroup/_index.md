---
title: RevisionGroup class
linktitle: RevisionGroup class
articleTitle: RevisionGroup class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.RevisionGroup class. Represents a group of sequential [Revision](../revision/) objects"
type: docs
weight: 1080
url: /nodejs-net/aspose.words/revisiongroup/
---

## RevisionGroup class

Represents a group of sequential [Revision](../revision/) objects.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/nodejs-net/track-changes-in-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [author](./author/) | Gets the author of this revision group. |
| [revisionType](./revisionType/) | Gets the type of revisions included in this group. |
| [text](./text/) | Returns inserted/deleted/moved text or description of format change. |

### Examples

Shows how to print info about a group of revisions in a document.

```js
let doc = new aw.Document(base.myDir + "Revisions.docx");

expect(doc.revisions.groups.count).toEqual(7);

for (let group of doc.revisions.groups)
{
  console.log(
    `Revision author: ${group.author}; Revision type: ${group.revisionType} \n\tRevision text: ${group.text}`);
}
```

### See Also

* module [Aspose.Words](../)

