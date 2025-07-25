﻿---
title: TableStyle.leftIndent property
linktitle: leftIndent property
articleTitle: leftIndent property
second_title: Aspose.Words for Node.js
description: "TableStyle.leftIndent property. Gets or sets the value that represents the left indent of a table."
type: docs
weight: 80
url: /nodejs-net/aspose.words/tablestyle/leftIndent/
---

## TableStyle.leftIndent property

Gets or sets the value that represents the left indent of a table.


```js
get leftIndent(): number
```

### Examples

Shows how to set the position of a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two ways of aligning a table horizontally.
// 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
let tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle1").asTableStyle();
tableStyle.alignment = aw.Tables.TableAlignment.Center;
tableStyle.borders.color = "#0000FF";
tableStyle.borders.lineStyle = aw.LineStyle.Single;

// Insert a table and apply the style we created to it.
let table = builder.startTable();
builder.insertCell();
builder.write("Aligned to the center of the page");
builder.endTable();
table.preferredWidth = aw.Tables.PreferredWidth.fromPoints(300);

table.style = tableStyle;

// 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle2").asTableStyle();
tableStyle.leftIndent = 55;
tableStyle.borders.color = "#008000";
tableStyle.borders.lineStyle = aw.LineStyle.Single;

table = builder.startTable();
builder.insertCell();
builder.write("Aligned according to left indent");
builder.endTable();
table.preferredWidth = aw.Tables.PreferredWidth.fromPoints(300);

table.style = tableStyle;

doc.save(base.artifactsDir + "Table.SetTableAlignment.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TableStyle](../)

