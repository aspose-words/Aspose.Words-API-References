---
title: ConditionalStyleType enumeration
linktitle: ConditionalStyleType enumeration
articleTitle: ConditionalStyleType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.ConditionalStyleType enumeration. Represents possible table areas to which conditional formatting may be defined in a table style."
type: docs
weight: 260
url: /nodejs-net/aspose.words/conditionalstyletype/
---

## ConditionalStyleType enumeration

Represents possible table areas to which conditional formatting may be defined in a table style.


### Members

| Name | Description |
| --- | --- |
| FirstRow | Specifies formatting of the first row of a table. |
| FirstColumn | Specifies formatting of the first column of a table. |
| LastRow | Specifies formatting of the last row of a table. |
| LastColumn | Specifies formatting of the last column of a table. |
| OddRowBanding | Specifies formatting of odd-numbered row stripe. |
| OddColumnBanding | Specifies formatting of odd-numbered column stripe. |
| EvenRowBanding | Specifies formatting of even-numbered row stripe. |
| EvenColumnBanding | Specifies formatting of even-numbered column stripe. |
| TopLeftCell | Specifies formatting of the top left cell of a table. |
| TopRightCell | Specifies formatting of the top right cell of a table. |
| BottomLeftCell | Specifies formatting of the bottom left cell of a table. |
| BottomRightCell | Specifies formatting of the bottom right cell of a table. |

### Examples

Shows how to work with certain area styles of a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Cell 1");
builder.insertCell();
builder.write("Cell 2");
builder.endRow();
builder.insertCell();
builder.write("Cell 3");
builder.insertCell();
builder.write("Cell 4");
builder.endTable();

// Create a custom table style.
let tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle1").asTableStyle();

// Conditional styles are formatting changes that affect only some of the table's cells
// based on a predicate, such as the cells being in the last row.
// Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
// 1 -  By style type:
tableStyle.conditionalStyles.at(aw.ConditionalStyleType.FirstRow).shading.backgroundPatternColor = "#F0F8FF";

// 2 -  By index:
tableStyle.conditionalStyles.at(0).borders.color = "#000000";
tableStyle.conditionalStyles.at(0).borders.lineStyle = aw.LineStyle.DotDash;
expect(tableStyle.conditionalStyles.at(0).type).toEqual(aw.ConditionalStyleType.FirstRow);

// 3 -  As a property:
tableStyle.conditionalStyles.firstRow.paragraphFormat.alignment = aw.ParagraphAlignment.Center;

// Apply padding and text formatting to conditional styles.
tableStyle.conditionalStyles.lastRow.bottomPadding = 10;
tableStyle.conditionalStyles.lastRow.leftPadding = 10;
tableStyle.conditionalStyles.lastRow.rightPadding = 10;
tableStyle.conditionalStyles.lastRow.topPadding = 10;
tableStyle.conditionalStyles.lastColumn.font.bold = true;

// List all possible style conditions.
for (var currentStyle of tableStyle.conditionalStyles)
{
    if (currentStyle != null) console.log(currentStyle.type);
}

// Apply the custom style, which contains all conditional styles, to the table.
table.style = tableStyle;

// Our style applies some conditional styles by default.
expect(table.styleOptions).toEqual(aw.Tables.TableStyleOptions.FirstRow | aw.Tables.TableStyleOptions.FirstColumn | aw.Tables.TableStyleOptions.RowBands);

// We will need to enable all other styles ourselves via the "StyleOptions" property.
table.styleOptions = table.styleOptions | aw.Tables.TableStyleOptions.LastRow | aw.Tables.TableStyleOptions.LastColumn;

doc.save(base.artifactsDir + "Table.conditionalStyles.docx");
```

### See Also

* module [Aspose.Words](../)

