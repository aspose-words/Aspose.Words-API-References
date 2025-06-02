---
title: MultiPageLayout.Grid
linktitle: Grid
articleTitle: Grid
second_title: Aspose.Words for .NET
description: Arranges pages left to right, top to bottom in a grid layout for compact multi-page image output.
type: docs
weight: 30
url: /net/aspose.words.saving/multipagelayout/grid/
---
## MultiPageLayout.Grid method

Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the specified number of columns.

```csharp
public static MultiPageLayout Grid(int columns, float horizontalGap, float verticalGap)
```

| Parameter | Type | Description |
| --- | --- | --- |
| columns | Int32 | The number of columns in the layout. Must be greater than zero. |
| horizontalGap | Single | The horizontal gap between columns in points. |
| verticalGap | Single | The vertical gap between rows in points. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Thrown if *columns* is less than or equal to zero. |

### See Also

* class [MultiPageLayout](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
