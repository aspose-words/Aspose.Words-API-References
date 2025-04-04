---
title: Bookmark.firstColumn property
linktitle: firstColumn property
articleTitle: firstColumn property
second_title: Aspose.Words for Node.js
description: "Bookmark.firstColumn property. Gets the zero-based index of the first column of the table column range associated with the bookmark."
type: docs
weight: 30
url: /nodejs-net/aspose.words/bookmark/firstColumn/
---

## Bookmark.firstColumn property

Gets the zero-based index of the first column of the table column range associated with the bookmark.


```js
get firstColumn(): number
```

### Remarks

Returns **-1** if this bookmark is not a table column bookmark.



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

