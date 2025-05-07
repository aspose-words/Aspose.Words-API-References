---
title: TextColumnCollection.setCount method
linktitle: setCount method
articleTitle: setCount method
second_title: Aspose.Words for Node.js
description: "TextColumnCollection.setCount method. Arranges text into the specified number of text columns."
type: docs
weight: 70
url: /nodejs-net/aspose.words/textcolumncollection/setCount/
---

## setCount(newCount) {#number}

Arranges text into the specified number of text columns.


```js
setCount(newCount: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| newCount | number | The number of columns the text is to be arranged into. |

### Remarks

When [TextColumnCollection.evenlySpaced](../evenlySpaced/) is ``false`` and you increase the number of columns,
new [TextColumn](../../textcolumn/) objects are created with zero width and spacing.
You need to set width and spacing for the new columns.




### Examples

Shows how to create multiple evenly spaced columns in a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let columns = builder.pageSetup.textColumns;
columns.spacing = 100;
columns.setCount(2);

builder.writeln("Column 1.");
builder.insertBreak(aw.BreakType.ColumnBreak);
builder.writeln("Column 2.");

doc.save(base.artifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TextColumnCollection](../)

