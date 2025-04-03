---
title: Bookmark.isColumn property
linktitle: isColumn property
articleTitle: isColumn property
second_title: Aspose.Words for NodeJs
description: "Bookmark.isColumn property. Returns ``true`` if this bookmark is a table column bookmark."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/bookmark/isColumn/
---

## Bookmark.isColumn property

Returns ``true`` if this bookmark is a table column bookmark.



```js
get isColumn(): boolean
```

### Examples

Shows how to get information about table column bookmarks.

```js
var doc = new aw.Document(base.myDir + "Table column bookmarks.doc");

for (let bookmark of doc.range.bookmarks)
{
  console.log(`Bookmark: ${bookmark.name}${(bookmark.isColumn ? " (Column)" : "")}`);
}
```

### See Also

* module [Aspose.Words](../../)
* class [Bookmark](../)

