---
title: TextColumnCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Node.js
description: "TextColumnCollection.count property. Gets the number of columns in the section of a document."
type: docs
weight: 10
url: /nodejs-net/aspose.words/textcolumncollection/count/
---

## TextColumnCollection.count property

Gets the number of columns in the section of a document.


```js
get count(): number
```

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

