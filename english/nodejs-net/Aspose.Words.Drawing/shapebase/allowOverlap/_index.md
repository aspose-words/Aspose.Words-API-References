---
title: ShapeBase.allowOverlap property
linktitle: allowOverlap property
articleTitle: allowOverlap property
second_title: Aspose.Words for Node.js
description: "ShapeBase.allowOverlap property. Gets or sets a value that specifies whether this shape can overlap other shapes."
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing/shapebase/allowOverlap/
---

## ShapeBase.allowOverlap property

Gets or sets a value that specifies whether this shape can overlap other shapes.


```js
get allowOverlap(): boolean
```

### Remarks

This property affects behavior of the shape in Microsoft Word.
Aspose.Words ignores the value of this property.

This property is applicable only to top level shapes.

The default value is ``true``.




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

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

