---
title: Table.distanceLeft property
linktitle: distanceLeft property
articleTitle: distanceLeft property
second_title: Aspose.Words for NodeJs
description: "Table.distanceLeft property. Gets or sets distance between table left and the surrounding text, in points."
type: docs
weight: 130
url: /nodejs-net/aspose.words/table/distanceLeft/
---

## Table.distanceLeft property

Gets or sets distance between table left and the surrounding text, in points.


```js
get distanceLeft(): number
```

### Examples

Shows how to set distance between table boundaries and text.

```js
let doc = new aw.Document(base.myDir + "Table wrapped by text.docx");

let table = doc.firstSection.body.tables.at(0);
expect(table.distanceTop).toEqual(25.9);
expect(table.distanceBottom).toEqual(25.9);
expect(table.distanceLeft).toEqual(17.3);
expect(table.distanceRight).toEqual(17.3);

// Set distance between table and surrounding text.
table.distanceLeft = 24;
table.distanceRight = 24;
table.distanceTop = 3;
table.distanceBottom = 3;

doc.save(base.artifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

