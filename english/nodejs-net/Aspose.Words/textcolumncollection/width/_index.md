---
title: TextColumnCollection.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Node.js
description: "TextColumnCollection.width property. When columns are evenly spaced, gets the width of the columns."
type: docs
weight: 60
url: /nodejs-net/aspose.words/textcolumncollection/width/
---

## TextColumnCollection.width property

When columns are evenly spaced, gets the width of the columns.


```js
get width(): number
```

### Remarks

Has effect only when [TextColumnCollection.evenlySpaced](../evenlySpaced/) is set to ``true``.




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

