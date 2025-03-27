---
title: RevisionGroup.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for NodeJs
description: "RevisionGroup.text property. Returns inserted/deleted/moved text or description of format change."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words/revisiongroup/text/
---

## RevisionGroup.text property

Returns inserted/deleted/moved text or description of format change.


```js
get text(): string
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

