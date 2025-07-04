---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: Discover the Table EnsureMinimum method, effortlessly create and append a row when your table is empty for seamless data management.
type: docs
weight: 420
url: /net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

If the table has no rows, creates and appends one [`Row`](../../row/).

```csharp
public void EnsureMinimum()
```

## Examples

Shows how to ensure that a table node contains the nodes we need to add content.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tables contain rows, which contain cells, which may contain paragraphs
// with typical elements such as runs, shapes, and even other tables.
// Our new table has none of these nodes, and we cannot add contents to it until it does.
Assert.That(table.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(0));

// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one row and one cell with an empty paragraph.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### See Also

* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
