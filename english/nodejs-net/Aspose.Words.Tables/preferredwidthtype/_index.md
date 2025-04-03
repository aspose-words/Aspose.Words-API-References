---
title: PreferredWidthType enumeration
linktitle: PreferredWidthType enumeration
articleTitle: PreferredWidthType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Tables.PreferredWidthType enumeration. Specifies the unit of measurement for the preferred width of a table or cell."
type: docs
weight: 80
url: /nodejs-net/aspose.words.tables/preferredwidthtype/
---

## PreferredWidthType enumeration

Specifies the unit of measurement for the preferred width of a table or cell.


### Members

| Name | Description |
| --- | --- |
| Auto | The preferred width is not specified. The actual width of the table or cell is either specified using the explicit width or  will be determined automatically by the table layout algorithm when the table is displayed, depending on the table auto fit setting. |
| Percent | Measure the current item width using a specified percentage. |
| Points | Measure the current item width using a specified number of points (1/72 inch). |

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

* module [Aspose.Words.Tables](../)
* class [PreferredWidth](../preferredwidth/)

