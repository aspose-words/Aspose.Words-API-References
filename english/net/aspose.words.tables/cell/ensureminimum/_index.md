---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: Optimize your cell structure with the EnsureMinimum method, effortlessly add a paragraph if the last child isn't one. Enhance your document's clarity!
type: docs
weight: 160
url: /net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

If the last child is not a paragraph, creates and appends one empty paragraph.

```csharp
public void EnsureMinimum()
```

## Examples

Shows how to ensure a cell node contains the nodes we need to begin adding content to it.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Cells may contain paragraphs with typical elements such as runs, shapes, and even other tables.
// Our new cell does not have any paragraphs, and we cannot add contents such as run and shape nodes to it until it does.
Assert.That(cell.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(0));

// Calling the "EnsureMinimum" method on a cell will ensure that
// the cell has at least one empty paragraph, which we can then add contents to.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### See Also

* class [Cell](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
