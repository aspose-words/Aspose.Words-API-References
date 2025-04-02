---
title: ConditionalStyle.clearFormatting method
linktitle: clearFormatting method
articleTitle: clearFormatting method
second_title: Aspose.Words for NodeJs
description: "ConditionalStyle.clearFormatting method. Clears formatting of this conditional style."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words/conditionalstyle/clearFormatting/
---

## clearFormatting() {#default}

Clears formatting of this conditional style.


```js
clearFormatting()
```

### Examples

Shows how to reset conditional table styles.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("First row");
builder.endRow();
builder.insertCell();
builder.write("Last row");
builder.endTable();

let tableStyle = doc.styles.add(aw.StyleType.Table, "MyTableStyle1").asTableStyle();
table.style = tableStyle;

// Set the table style to color the borders of the first row of the table in red.
tableStyle.conditionalStyles.firstRow.borders.color = "#FF0000";

// Set the table style to color the borders of the last row of the table in blue.
tableStyle.conditionalStyles.lastRow.borders.color = "#0000FF";

// Below are two ways of using the "ClearFormatting" method to clear the conditional styles.
// 1 -  Clear the conditional styles for a specific part of a table:
tableStyle.conditionalStyles.at(0).clearFormatting();

expect(tableStyle.conditionalStyles.firstRow.borders.color).toEqual(base.emptyColor);

// 2 -  Clear the conditional styles for the entire table:
tableStyle.conditionalStyles.clearFormatting();

expect([...tableStyle.conditionalStyles].every(s => s.borders.color == "")).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [ConditionalStyle](../)

