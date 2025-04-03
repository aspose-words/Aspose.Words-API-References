---
title: Table.allowOverlap property
linktitle: allowOverlap property
articleTitle: allowOverlap property
second_title: Aspose.Words for NodeJs
description: "Table.allowOverlap property. Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed"
type: docs
weight: 70
url: /nodejs-net/aspose.words/table/allowOverlap/
---

## Table.allowOverlap property

Gets whether a floating table shall allow other floating objects in the document
to overlap its extents when displayed.
Default value is ``true``.



```js
get allowOverlap(): boolean
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

