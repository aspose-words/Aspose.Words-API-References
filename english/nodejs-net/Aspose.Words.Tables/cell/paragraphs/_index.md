---
title: Cell.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for NodeJs
description: "Cell.paragraphs property. Gets a collection of paragraphs that are immediate children of the cell."
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Tables/cell/paragraphs/
---

## Cell.paragraphs property

Gets a collection of paragraphs that are immediate children of the cell.


```js
get paragraphs(): Aspose.Words.ParagraphCollection
```

### Examples

Shows how to set a table to stay together on the same page.

```js
let doc = new aw.Document(base.myDir + "Table spanning two pages.docx");
let table = doc.firstSection.body.tables.at(0);

// Enabling KeepWithNext for every paragraph in the table except for the
// last ones in the last row will prevent the table from splitting across multiple pages.
for (var cellNode of table.getChildNodes(aw.NodeType.Cell, true)) {
  var cell = cellNode.asCell();
  for (let para of cell.paragraphs.toArray())
  {
    expect(para.isInCell).toEqual(true);

    if (!(cell.parentRow.isLastRow && para.isEndOfCell))
      para.paragraphFormat.keepWithNext = true;
  }
}

doc.save(base.artifactsDir + "Table.KeepTableTogether.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [Cell](../)

