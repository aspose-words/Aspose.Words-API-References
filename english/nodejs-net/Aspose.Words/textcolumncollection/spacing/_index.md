---
title: TextColumnCollection.spacing property
linktitle: spacing property
articleTitle: spacing property
second_title: Aspose.Words for Node.js
description: "TextColumnCollection.spacing property. When columns are evenly spaced, gets or sets the amount of space between each column in points."
type: docs
weight: 40
url: /nodejs-net/aspose.words/textcolumncollection/spacing/
---

## TextColumnCollection.spacing property

When columns are evenly spaced, gets or sets the amount of space between each column in points.


```js
get spacing(): number
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

