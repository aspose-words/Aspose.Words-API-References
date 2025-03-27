---
title: BorderCollection.horizontal property
linktitle: horizontal property
articleTitle: horizontal property
second_title: Aspose.Words for NodeJs
description: "BorderCollection.horizontal property. Gets the horizontal border that is used between cells or conforming paragraphs."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/bordercollection/horizontal/
---

## BorderCollection.horizontal property

Gets the horizontal border that is used between cells or conforming paragraphs.


```js
get horizontal(): Aspose.Words.Border
```

### Examples

Shows how to apply settings to horizontal borders to a paragraph's format.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a red horizontal border for the paragraph. Any paragraphs created afterwards will inherit these border settings.
let borders = doc.firstSection.body.firstParagraph.paragraphFormat.borders;
borders.horizontal.color = "#FF0000";
borders.horizontal.lineStyle = aw.LineStyle.DashSmallGap;
borders.horizontal.lineWidth = 3;

// Write text to the document without creating a new paragraph afterward.
// Since there is no paragraph underneath, the horizontal border will not be visible.
builder.write("Paragraph above horizontal border.");

// Once we add a second paragraph, the border of the first paragraph will become visible.
builder.insertParagraph();
builder.write("Paragraph below horizontal border.");

doc.save(base.artifactsDir + "Border.HorizontalBorders.docx");
```

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

