---
title: LayoutEnumerator class
linktitle: LayoutEnumerator class
articleTitle: LayoutEnumerator class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Layout.LayoutEnumerator class. Enumerates page layout entities of a document."
type: docs
weight: 60
url: /nodejs-net/aspose.words.layout/layoutenumerator/
---

## LayoutEnumerator class

Enumerates page layout entities of a document.

You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered,
as well as overall structure and relationships.
Use combination of Aspose.Words.Layout.LayoutCollector.GetEntity(Aspose.Words.Node) and Aspose.Words.Layout.LayoutEnumerator.Current move to the entity which corresponds to a document node.
To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/nodejs-net/converting-to-fixed-page-format/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [LayoutEnumerator(document)](./constructor/#document) | Initializes new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets document this instance enumerates. |
| [kind](./kind/) | Gets the kind of the current entity. This can be an empty string but never ``null``. |
| [pageIndex](./pageIndex/) | Gets the 1-based index of a page which contains the current entity. |
| [text](./text/) | Gets text of the current span entity. Throws for other entity types. |
| [this[]](./this[]/) |  |
| [type](./type/) | Gets the type of the current entity. |

### Methods

| Name | Description |
| --- | --- |
|[ moveFirstChild()](./moveFirstChild/#default) | Moves to the first child entity. |
|[ moveLastChild()](./moveLastChild/#default) | Moves to the last child entity. |
|[ moveNext()](./moveNext/#default) | Moves to the next sibling entity in visual order. |
|[ moveNextLogical()](./moveNextLogical/#default) | Moves to the next sibling entity in a logical order. |
|[ moveParent()](./moveParent/#default) | Moves to the parent entity. |
|[ moveParent(types)](./moveParent/#layoutentitytype) | Moves to the parent entity of the specified type. |
|[ movePrevious()](./movePrevious/#default) | Moves to the previous sibling entity. |
|[ movePreviousLogical()](./movePreviousLogical/#default) | Moves to the previous sibling entity in a logical order. |
|[ reset()](./reset/#default) | Moves the enumerator to the first page of the document. |

### See Also

* module [Aspose.Words.Layout](../)

