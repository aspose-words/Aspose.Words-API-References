---
title: CellFormat.setPaddings method
linktitle: setPaddings method
articleTitle: setPaddings method
second_title: Aspose.Words for Node.js
description: "CellFormat.setPaddings method. Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell."
type: docs
weight: 170
url: /nodejs-net/aspose.words.tables/cellformat/setPaddings/
---

## setPaddings(leftPadding, topPadding, rightPadding, bottomPadding) {#number_number_number_number}

Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell.


```js
setPaddings(leftPadding: number, topPadding: number, rightPadding: number, bottomPadding: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| leftPadding | number |  |
| topPadding | number |  |
| rightPadding | number |  |
| bottomPadding | number |  |

### Examples

Shows how to pad the contents of a cell with whitespace.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Set a padding distance (in points) between the border and the text contents
// of each table cell we create with the document builder. 
builder.cellFormat.setPaddings(5, 10, 40, 50);

// Create a table with one cell whose contents will have whitespace padding.
builder.startTable();
builder.insertCell();
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
      "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.save(base.artifactsDir + "CellFormat.Padding.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [CellFormat](../)

