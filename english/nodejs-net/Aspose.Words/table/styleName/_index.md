---
title: Table.styleName property
linktitle: styleName property
articleTitle: styleName property
second_title: Aspose.Words for Node.js
description: "Table.styleName property. Gets or sets the name of the table style applied to this table."
type: docs
weight: 290
url: /nodejs-net/aspose.words/table/styleName/
---

## Table.styleName property

Gets or sets the name of the table style applied to this table.


```js
get styleName(): string
```

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
    //expect(table.bidi).toEqual(true);
    expect(table.cellSpacing).toEqual(5.0);
    expect(table.styleName).toEqual("MyTableStyle1");

    doc.save(base.artifactsDir + "Table.TableStyleCreation.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

