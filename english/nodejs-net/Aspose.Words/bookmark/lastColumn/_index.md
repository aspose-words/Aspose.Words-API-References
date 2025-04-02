---
title: Bookmark.lastColumn property
linktitle: lastColumn property
articleTitle: lastColumn property
second_title: Aspose.Words for NodeJs
description: "Bookmark.lastColumn property. Gets the zero-based index of the last column of the table column range associated with the bookmark."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/bookmark/lastColumn/
---

## Bookmark.lastColumn property

Gets the zero-based index of the last column of the table column range associated with the bookmark.


```js
get lastColumn(): number
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

