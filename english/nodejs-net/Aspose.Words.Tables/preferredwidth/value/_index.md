---
title: PreferredWidth.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Node.js
description: "PreferredWidth.value property. Gets the preferred width value"
type: docs
weight: 20
url: /nodejs-net/aspose.words.tables/preferredwidth/value/
---

## PreferredWidth.value property

Gets the preferred width value. The unit of measure is specified in the [PreferredWidth.type](../type/) property.



```js
get value(): number
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

