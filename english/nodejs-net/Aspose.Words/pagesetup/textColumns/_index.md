---
title: PageSetup.textColumns property
linktitle: textColumns property
articleTitle: textColumns property
second_title: Aspose.Words for NodeJs
description: "PageSetup.textColumns property. Returns a collection that represents the set of text columns."
type: docs
weight: 420
url: /nodejs-net/aspose.words/pagesetup/textColumns/
---

## PageSetup.textColumns property

Returns a collection that represents the set of text columns.


```js
get textColumns(): Aspose.Words.TextColumnCollection
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
* class [PageSetup](../)

