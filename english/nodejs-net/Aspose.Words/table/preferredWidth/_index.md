---
title: Table.preferredWidth property
linktitle: preferredWidth property
articleTitle: preferredWidth property
second_title: Aspose.Words for NodeJs
description: "Table.preferredWidth property. Gets or sets the table preferred width."
type: docs
weight: 220
url: /nodejs-net/aspose.words/table/preferredWidth/
---

## Table.preferredWidth property

Gets or sets the table preferred width.


```js
get preferredWidth(): Aspose.Words.Tables.PreferredWidth
```

### Remarks

The default value is Aspose.Words.Tables.PreferredWidth.Auto.




### Examples

Shows how to set a table to auto fit to 50% of the width of the page.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Cell #1");
builder.insertCell();
builder.write("Cell #2");
builder.insertCell();
builder.write("Cell #3");

table.preferredWidth = aw.Tables.PreferredWidth.fromPercent(50);

doc.save(base.artifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

