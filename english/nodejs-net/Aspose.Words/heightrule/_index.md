---
title: HeightRule enumeration
linktitle: HeightRule enumeration
articleTitle: HeightRule enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.HeightRule enumeration. Specifies the rule for determining the height of an object."
type: docs
weight: 530
url: /nodejs-net/aspose.words/heightrule/
---

## HeightRule enumeration

Specifies the rule for determining the height of an object.


### Members

| Name | Description |
| --- | --- |
| AtLeast | The height will be at least the specified height in points. It will grow, if needed, to accommodate all text inside an object. |
| Exactly | The height is specified exactly in points. Please note that if the text cannot fit inside the object of this height, it will appear truncated. |
| Auto | The height will grow automatically to accommodate all text inside an object. |

### Examples

Shows how to format rows with a document builder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Row 1, cell 1.");

// Start a second row, and then configure its height. The builder will apply these settings to
// its current row, as well as any new rows it creates afterwards.
builder.endRow();

let rowFormat = builder.rowFormat;
rowFormat.height = 100;
rowFormat.heightRule = aw.HeightRule.Exactly;

builder.insertCell();
builder.write("Row 2, cell 1.");
builder.endTable();

// The first row was unaffected by the padding reconfiguration and still holds the default values.
expect(table.rows.at(0).rowFormat.height).toEqual(0.0);
expect(table.rows.at(0).rowFormat.heightRule).toEqual(aw.HeightRule.Auto);

expect(table.rows.at(1).rowFormat.height).toEqual(100.0);
expect(table.rows.at(1).rowFormat.heightRule).toEqual(aw.HeightRule.Exactly);

doc.save(base.artifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### See Also

* module [Aspose.Words](../)

