---
title: PreferredWidth.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for NodeJs
description: "PreferredWidth.type property. Gets the unit of measure used for this preferred width value."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Tables/preferredwidth/type/
---

## PreferredWidth.type property

Gets the unit of measure used for this preferred width value.


```js
get type(): Aspose.Words.Tables.PreferredWidthType
```

### Examples

Shows how to verify the preferred width type and value of a table cell.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

let table = doc.firstSection.body.tables.at(0);
let firstCell = table.firstRow.firstCell;

expect(firstCell.cellFormat.preferredWidth.type).toEqual(aw.Tables.PreferredWidthType.Percent);
expect(firstCell.cellFormat.preferredWidth.value).toEqual(11.16);
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [PreferredWidth](../)

