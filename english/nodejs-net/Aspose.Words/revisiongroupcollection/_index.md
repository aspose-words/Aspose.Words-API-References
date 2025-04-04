---
title: RevisionGroupCollection class
linktitle: RevisionGroupCollection class
articleTitle: RevisionGroupCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.RevisionGroupCollection class. A collection of [RevisionGroup](../revisiongroup/) objects that represent revision groups in the document"
type: docs
weight: 1100
url: /nodejs-net/aspose.words/revisiongroupcollection/
---

## RevisionGroupCollection class

A collection of [RevisionGroup](../revisiongroup/) objects that represent revision groups in the document.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/nodejs-net/track-changes-in-a-document/) documentation article.




### Remarks

You do not create instances of this class directly. Use the [RevisionCollection.groups](../revisioncollection/groups/)
property to get revision groups present in a document.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of revision groups in the collection. |
| [this[]](./this[]/) |  |

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

Shows how to get a group of revisions in a document.

```js
let doc = new aw.Document(base.myDir + "Revisions.docx");

let revisionGroup = doc.revisions.groups.at(0);
```

### See Also

* module [Aspose.Words](../)

