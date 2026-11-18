---
title: Aspose::Words::Layout::LayoutEnumerator::MovePreviousLogical method
linktitle: MovePreviousLogical
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutEnumerator::MovePreviousLogical method. Moves to the previous sibling entity in a logical order. When iterating lines of a paragraph broken across pages this method will move to the previous line even if it resides on another page in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.layout/layoutenumerator/movepreviouslogical/
---
## LayoutEnumerator::MovePreviousLogical method


Moves to the previous sibling entity in a logical order. When iterating lines of a paragraph broken across pages this method will move to the previous line even if it resides on another page.

```cpp
_Bool Aspose::Words::Layout::LayoutEnumerator::MovePreviousLogical()
```

## Remarks

 Note that all [Span](../../layoutentitytype/) entities are linked together thus if [Current](../get_current/) entity is span repeated calling of this method will iterates complete story of the document. 
## See Also

* Class [LayoutEnumerator](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
