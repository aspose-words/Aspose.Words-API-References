---
title: ConditionalStyle.shading property
linktitle: shading property
articleTitle: shading property
second_title: Aspose.Words for NodeJs
description: "ConditionalStyle.shading property. Gets a [Shading](../../shading/) object that refers to the shading formatting for this conditional style."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words/conditionalstyle/shading/
---

## ConditionalStyle.shading property

Gets a [Shading](../../shading/) object that refers to the shading formatting for this conditional style.



```js
get shading(): Aspose.Words.Shading
```

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

* module [Aspose.Words](../../)
* class [ConditionalStyle](../)

