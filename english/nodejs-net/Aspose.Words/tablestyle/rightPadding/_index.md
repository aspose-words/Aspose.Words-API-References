﻿---
title: TableStyle.rightPadding property
linktitle: rightPadding property
articleTitle: rightPadding property
second_title: Aspose.Words for Node.js
description: "TableStyle.rightPadding property. Gets or sets the amount of space (in points) to add to the right of the contents of table cells."
type: docs
weight: 100
url: /nodejs-net/aspose.words/tablestyle/rightPadding/
---

## TableStyle.rightPadding property

Gets or sets the amount of space (in points) to add to the right of the contents of table cells.


```js
get rightPadding(): number
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
    expect(table.bidi).toEqual(true);
    expect(table.cellSpacing).toEqual(5.0);
    expect(table.styleName).toEqual("MyTableStyle1");

    doc.save(base.artifactsDir + "Table.TableStyleCreation.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TableStyle](../)

