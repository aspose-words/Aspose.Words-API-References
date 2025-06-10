---
title: LayoutEnumerator.moveNextLogical method
linktitle: moveNextLogical method
articleTitle: moveNextLogical method
second_title: Aspose.Words for Node.js
description: "LayoutEnumerator.moveNextLogical method. Moves to the next sibling entity in a logical order."
type: docs
weight: 110
url: /nodejs-net/aspose.words.layout/layoutenumerator/moveNextLogical/
---

## moveNextLogical() {#default}

Moves to the next sibling entity in a logical order.

When iterating lines of a paragraph broken across pages this method
will move to the next line even if it resides on another page.


```js
moveNextLogical()
```

### Remarks

Note that all [LayoutEntityType.Span](../../layoutentitytype/#Span) entities are linked together thus if Aspose.Words.Layout.LayoutEnumerator.Current
entity is span repeated calling of this method will iterates complete story of the document.



### See Also

* module [Aspose.Words.Layout](../../)
* class [LayoutEnumerator](../)

