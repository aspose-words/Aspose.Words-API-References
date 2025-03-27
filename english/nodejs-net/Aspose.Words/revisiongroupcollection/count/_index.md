---
title: RevisionGroupCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for NodeJs
description: "RevisionGroupCollection.count property. Returns the number of revision groups in the collection."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/revisiongroupcollection/count/
---

## RevisionGroupCollection.count property

Returns the number of revision groups in the collection.


```js
get count(): number
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
* class [RevisionGroupCollection](../)

