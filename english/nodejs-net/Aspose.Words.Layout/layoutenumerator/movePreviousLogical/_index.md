---
title: LayoutEnumerator.movePreviousLogical method
linktitle: movePreviousLogical method
articleTitle: movePreviousLogical method
second_title: Aspose.Words for Node.js
description: "LayoutEnumerator.movePreviousLogical method. Moves to the previous sibling entity in a logical order."
type: docs
weight: 140
url: /nodejs-net/aspose.words.layout/layoutenumerator/movePreviousLogical/
---

## movePreviousLogical() {#default}

Moves to the previous sibling entity in a logical order.

When iterating lines of a paragraph broken across pages this method
will move to the previous line even if it resides on another page.


```js
movePreviousLogical()
```

### Remarks

Note that all [LayoutEntityType.Span](../../layoutentitytype/#Span) entities are linked together thus if Aspose.Words.Layout.LayoutEnumerator.Current
entity is span repeated calling of this method will iterates complete story of the document.



### See Also

* module [Aspose.Words.Layout](../../)
* class [LayoutEnumerator](../)

