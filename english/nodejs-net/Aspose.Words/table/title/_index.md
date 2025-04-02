---
title: Table.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for NodeJs
description: "Table.title property. Gets or sets title of this table"
type: docs
weight: 320
url: /nodejs-net/Aspose.Words/table/title/
---

## Table.title property

Gets or sets title of this table.
It provides an alternative text representation of the information contained in the table.


```js
get title(): string
```

### Remarks

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents
([OoxmlCompliance](../../../Aspose.Words.Saving/ooxmlcompliance/)).
When saved to pre-ISO/IEC 29500 formats, the property is ignored.




### Examples

Shows how to build a nested table without using a document builder.

```js
test('CreateNestedTable', () => {
  let doc = new aw.Document();

  // Create the outer table with three rows and four columns, and then add it to the document.
  let outerTable = createTable(doc, 3, 4, "Outer Table");
  doc.firstSection.body.appendChild(outerTable);

  // Create another table with two rows and two columns and then insert it into the first table's first cell.
  let innerTable = createTable(doc, 2, 2, "Inner Table");
  outerTable.firstRow.firstCell.appendChild(innerTable);

  doc.save(base.artifactsDir + "Table.CreateNestedTable.docx");
});


/// <summary>
/// Creates a new table in the document with the given dimensions and text in each cell.
/// </summary>
function createTable(doc, rowCount, cellCount, cellText)
{
  let table = new aw.Tables.Table(doc);

  for (let rowId = 1; rowId <= rowCount; rowId++)
  {
    let row = new aw.Tables.Row(doc);
    table.appendChild(row);

    for (let cellId = 1; cellId <= cellCount; cellId++)
    {
      let cell = new aw.Tables.Cell(doc);
      cell.appendChild(new aw.Paragraph(doc));
      cell.firstParagraph.appendChild(new aw.Run(doc, cellText));

      row.appendChild(cell);
    }
  }

  // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
  // The table must have at least one row before we can use these properties.
  // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
  // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
  table.title = "Aspose table title";
  table.description = "Aspose table description";

  return table;
}
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

