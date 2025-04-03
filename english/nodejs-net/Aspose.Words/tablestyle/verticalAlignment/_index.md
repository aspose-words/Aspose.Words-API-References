---
title: TableStyle.verticalAlignment property
linktitle: verticalAlignment property
articleTitle: verticalAlignment property
second_title: Aspose.Words for NodeJs
description: "TableStyle.verticalAlignment property. Specifies the vertical alignment for the cells."
type: docs
weight: 150
url: /nodejs-net/aspose.words/tablestyle/verticalAlignment/
---

## TableStyle.verticalAlignment property

Specifies the vertical alignment for the cells.


```js
get verticalAlignment(): Aspose.Words.Tables.CellVerticalAlignment
```

### Remarks

The default value is [CellVerticalAlignment.Top](../../../aspose.words.tables/cellverticalalignment/#Top).



### Examples

Shows how to create custom style settings for the table.

```js
let doc = new aw.Document();
    let builder = new aw.DocumentBuilder(doc);
 
    let table = builder.startTable();
    builder.insertCell();
    builder.write("Name");
    builder.insertCell();
    builder.write("مرحبًا");
    builder.endRow();
    builder.insertCell();
    builder.insertCell();
    builder.endTable();
 
    let tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle1").asTableStyle();
    tableStyle.allowBreakAcrossPages = true;
    tableStyle.bidi = true;
    tableStyle.cellSpacing = 5;
    tableStyle.bottomPadding = 20;
    tableStyle.leftPadding = 5;
    tableStyle.rightPadding = 10;
    tableStyle.topPadding = 20;
    tableStyle.shading.backgroundPatternColor = "#FAEBD7";
    tableStyle.borders.color = "#0000FF";
    tableStyle.borders.lineStyle = aw.LineStyle.DotDash;
    tableStyle.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;

    table.style = tableStyle;

    // Setting the style properties of a table may affect the properties of the table itself.
    expect(table.bidi).toEqual(true);
    expect(table.cellSpacing).toEqual(5.0);
    expect(table.styleName).toEqual("MyTableStyle1");

    doc.save(base.artifactsDir + "Table.TableStyleCreation.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TableStyle](../)

