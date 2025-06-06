﻿---
title: RevisionCollection.rejectAll method
linktitle: rejectAll method
articleTitle: rejectAll method
second_title: Aspose.Words for Node.js
description: "RevisionCollection.rejectAll method. Rejects all revisions in this collection."
type: docs
weight: 70
url: /nodejs-net/aspose.words/revisioncollection/rejectAll/
---

## rejectAll() {#default}

Rejects all revisions in this collection.


```js
rejectAll()
```

### Examples

Shows how to work with a document's collection of revisions.

```js
let doc = new aw.Document(base.myDir + "Revisions.docx");
let revisions = doc.revisions;

// This collection itself has a collection of revision groups.
// Each group is a sequence of adjacent revisions.
expect(revisions.groups.count).toEqual(7);
console.log(`${revisions.groups.count} revision groups:`);

// Iterate over the collection of groups and print the text that the revision concerns.
using (IEnumerator<RevisionGroup> e = revisions.groups.getEnumerator())
{
  while (e.moveNext())
  {
    console.log(`\tGroup type \"${e.current.revisionType}\", ` +
            `author: ${e.current.author}, contents: [${e.current.text.trim()}]`);
  }
}

// Each Run that a revision affects gets a corresponding Revision object.
// The revisions' collection is considerably larger than the condensed form we printed above,
// depending on how many Runs we have segmented the document into during Microsoft Word editing.
expect(revisions.count).toEqual(11);
console.log(`\n${revisions.count} revisions:`);

using (IEnumerator<Revision> e = revisions.getEnumerator())
{
  while (e.moveNext())
  {
    // A StyleDefinitionChange strictly affects styles and not document nodes. This means the "ParentStyle"
    // property will always be in use, while the ParentNode will always be null.
    // Since all other changes affect nodes, ParentNode will conversely be in use, and ParentStyle will be null.
    if (e.current.revisionType == aw.RevisionType.StyleDefinitionChange)
    {
      console.log(`\tRevision type \"${e.current.revisionType}\", ` +
              `author: ${e.current.author}, style: [${e.current.parentStyle.name}]`);
    }
    else
    {
      console.log(`\tRevision type \"${e.current.revisionType}\", ` +
              `author: ${e.current.author}, contents: [${e.current.parentNode.getText().trim()}]`);
    }
  }
}

// Reject all revisions via the collection, reverting the document to its original form.
revisions.rejectAll();

expect(revisions.count).toEqual(0);
```

### See Also

* module [Aspose.Words](../../)
* class [RevisionCollection](../)

