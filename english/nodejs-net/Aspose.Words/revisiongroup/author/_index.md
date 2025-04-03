---
title: RevisionGroup.author property
linktitle: author property
articleTitle: author property
second_title: Aspose.Words for NodeJs
description: "RevisionGroup.author property. Gets the author of this revision group."
type: docs
weight: 10
url: /nodejs-net/aspose.words/revisiongroup/author/
---

## RevisionGroup.author property

Gets the author of this revision group.


```js
get author(): string
```

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

* module [Aspose.Words](../../)
* class [RevisionGroup](../)

