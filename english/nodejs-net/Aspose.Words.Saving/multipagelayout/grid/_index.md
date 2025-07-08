---
title: MultiPageLayout.grid method
linktitle: grid method
articleTitle: grid method
second_title: Aspose.Words for Node.js
description: "MultiPageLayout.grid method. Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the specified number of columns."
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/multipagelayout/grid/
---

## grid(columns, horizontalGap, verticalGap) {#number_number_number}

Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the
specified number of columns.


```js
grid(columns: number, horizontalGap: number, verticalGap: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| columns | number | The number of columns in the layout. Must be greater than zero. |
| horizontalGap | number | The horizontal gap between columns in points. |
| verticalGap | number | The vertical gap between rows in points. |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Thrown if *columns* is less than or equal to zero. |

### See Also

* module [Aspose.Words.Saving](../../)
* class [MultiPageLayout](../)

