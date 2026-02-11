---
title: ConditionalStyle class
linktitle: ConditionalStyle class
articleTitle: ConditionalStyle class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.ConditionalStyle class. Represents special formatting applied to some area of a table with assigned table style"
type: docs
weight: 250
url: /nodejs-net/aspose.words/conditionalstyle/
---

## ConditionalStyle class

Represents special formatting applied to some area of a table with assigned table style.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/nodejs-net/working-with-tables/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [borders](./borders/) | Gets the collection of default cell borders for the conditional style. |
| [bottomPadding](./bottomPadding/) | Gets or sets the amount of space (in points) to add below the contents of table cells. |
| [font](./font/) | Gets the character formatting of the conditional style. |
| [leftPadding](./leftPadding/) | Gets or sets the amount of space (in points) to add to the left of the contents of table cells. |
| [paragraphFormat](./paragraphFormat/) | Gets the paragraph formatting of the conditional style. |
| [rightPadding](./rightPadding/) | Gets or sets the amount of space (in points) to add to the right of the contents of table cells. |
| [shading](./shading/) | Gets a [Shading](../shading/) object that refers to the shading formatting for this conditional style. |
| [topPadding](./topPadding/) | Gets or sets the amount of space (in points) to add above the contents of table cells. |
| [type](./type/) | Gets table area to which this conditional style relates. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Clears formatting of this conditional style. |

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

