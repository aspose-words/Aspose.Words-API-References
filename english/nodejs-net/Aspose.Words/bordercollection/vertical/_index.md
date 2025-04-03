---
title: BorderCollection.vertical property
linktitle: vertical property
articleTitle: vertical property
second_title: Aspose.Words for NodeJs
description: "BorderCollection.vertical property. Gets the vertical border that is used between cells."
type: docs
weight: 140
url: /nodejs-net/aspose.words/bordercollection/vertical/
---

## BorderCollection.vertical property

Gets the vertical border that is used between cells.


```js
get vertical(): Aspose.Words.Border
```

### Examples

Shows how to apply settings to vertical borders to a table row's format.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a table with red and blue inner borders.
let table = builder.startTable();

for (let i = 0; i < 3; i++)
{
  builder.insertCell();
  builder.write(`Row ${i + 1}, Column 1`);
  builder.insertCell();
  builder.write(`Row ${i + 1}, Column 2`);

  let row = builder.endRow();
  let borders = row.rowFormat.borders;

  // Adjust the appearance of borders that will appear between rows.
  borders.horizontal.color = "#FF0000";
  borders.horizontal.lineStyle = aw.LineStyle.Dot;
  borders.horizontal.lineWidth = 2.0;

  // Adjust the appearance of borders that will appear between cells.
  borders.vertical.color = "#0000FF";
  borders.vertical.lineStyle = aw.LineStyle.Dot;
  borders.vertical.lineWidth = 2.0;
}

// A row format, and a cell's inner paragraph use different border settings.
let border = table.firstRow.firstCell.lastParagraph.paragraphFormat.borders.vertical;

expect(border.color).toEqual(base.emptyColor);
expect(border.lineWidth).toEqual(0.0);
expect(border.lineStyle).toEqual(aw.LineStyle.None);

doc.save(base.artifactsDir + "Border.VerticalBorders.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [BorderCollection](../)

