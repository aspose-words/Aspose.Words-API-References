---
title: RevisionGroup.revisionType property
linktitle: revisionType property
articleTitle: revisionType property
second_title: Aspose.Words for NodeJs
description: "RevisionGroup.revisionType property. Gets the type of revisions included in this group."
type: docs
weight: 20
url: /nodejs-net/aspose.words/revisiongroup/revisionType/
---

## RevisionGroup.revisionType property

Gets the type of revisions included in this group.


```js
get revisionType(): Aspose.Words.RevisionType
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

