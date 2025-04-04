---
title: Table.verticalAnchor property
linktitle: verticalAnchor property
articleTitle: verticalAnchor property
second_title: Aspose.Words for Node.js
description: "Table.verticalAnchor property. Gets the base object from which the vertical positioning of floating table should be calculated"
type: docs
weight: 340
url: /nodejs-net/aspose.words/table/verticalAnchor/
---

## Table.verticalAnchor property

Gets the base object from which the vertical positioning of floating table should be calculated.
Default value is [RelativeVerticalPosition.Margin](../../../aspose.words.drawing/relativeverticalposition/#Margin).



```js
get verticalAnchor(): Aspose.Words.Drawing.RelativeVerticalPosition
```

### Examples

Shows how to work with floating tables properties.

```js
let doc = new aw.Document(base.myDir + "Table wrapped by text.docx");

let table = doc.firstSection.body.tables.at(0);

if (table.textWrapping == aw.Tables.TextWrapping.Around)
{
  expect(table.horizontalAnchor).toEqual(aw.Drawing.RelativeHorizontalPosition.Margin);
  expect(table.verticalAnchor).toEqual(aw.Drawing.RelativeVerticalPosition.Paragraph);
  expect(table.allowOverlap).toEqual(false);

  // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
  // The ArgumentException will be thrown for any other values.
  table.horizontalAnchor = aw.Drawing.RelativeHorizontalPosition.Column;

  // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
  // The ArgumentException will be thrown for any other values.
  table.verticalAnchor = aw.Drawing.RelativeVerticalPosition.Page;
}
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

