---
title: Paragraph.isInCell property
linktitle: isInCell property
articleTitle: isInCell property
second_title: Aspose.Words for NodeJs
description: "Paragraph.isInCell property. True if this paragraph is an immediate child of [Cell](../../../aspose.words.tables/cell/); false otherwise."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words/paragraph/isInCell/
---

## Paragraph.isInCell property

True if this paragraph is an immediate child of [Cell](../../../aspose.words.tables/cell/); false otherwise.



```js
get isInCell(): boolean
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

* module [Aspose.Words](../../)
* class [Paragraph](../)

