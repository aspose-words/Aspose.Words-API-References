---
title: TableStyle.rowStripe property
linktitle: rowStripe property
articleTitle: rowStripe property
second_title: Aspose.Words for Node.js
description: "TableStyle.rowStripe property. Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding."
type: docs
weight: 120
url: /nodejs-net/aspose.words/tablestyle/rowStripe/
---

## TableStyle.rowStripe property

Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding.


```js
get rowStripe(): number
```

### Examples

Shows how to create conditional table styles that alternate between rows.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// We can configure a conditional style of a table to apply a different color to the row/column,
// based on whether the row/column is even or odd, creating an alternating color pattern.
// We can also apply a number n to the row/column banding,
// meaning that the color alternates after every n rows/columns instead of one.
// Create a table where single columns and rows will band the columns will banded in threes.
let table = builder.startTable();
for (let i = 0; i < 15; i++)
{
  for (let j = 0; j < 4; j++)
  {
    builder.insertCell();
    builder.writeln(`${(j % 2 == 0 ? "Even" : "Odd")} column.`);
    builder.write(`Row banding ${(i % 3 == 0 ? "start" : "continuation")}.`);
  }
  builder.endRow();
}
builder.endTable();

// Apply a line style to all the borders of the table.
let tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle1").asTableStyle();
tableStyle.borders.color = "#000000";
tableStyle.borders.lineStyle = aw.LineStyle.Double;

// Set the two colors, which will alternate over every 3 rows.
tableStyle.rowStripe = 3;
tableStyle.conditionalStyles.at(aw.ConditionalStyleType.OddRowBanding).shading.backgroundPatternColor = "#ADD8E6";
tableStyle.conditionalStyles.at(aw.ConditionalStyleType.EvenRowBanding).shading.backgroundPatternColor = "#E0FFFF";

// Set a color to apply to every even column, which will override any custom row coloring.
tableStyle.columnStripe = 1;
tableStyle.conditionalStyles.at(aw.ConditionalStyleType.EvenColumnBanding).shading.backgroundPatternColor = "#FFA07A";

table.style = tableStyle;

// The "StyleOptions" property enables row banding by default.
expect(table.styleOptions).toEqual(aw.Tables.TableStyleOptions.FirstRow | aw.Tables.TableStyleOptions.FirstColumn | aw.Tables.TableStyleOptions.RowBands);

// Use the "StyleOptions" property also to enable column banding.
table.styleOptions = table.styleOptions | aw.Tables.TableStyleOptions.ColumnBands;

doc.save(base.artifactsDir + "Table.AlternatingRowStyles.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TableStyle](../)

