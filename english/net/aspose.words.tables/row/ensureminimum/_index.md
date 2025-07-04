---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: Discover the Row EnsureMinimum method, effortlessly create and append a Cell when none exist, enhancing your data structure management.
type: docs
weight: 160
url: /net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

If the [`Row`](../) has no cells, creates and appends one [`Cell`](../../cell/).

```csharp
public void EnsureMinimum()
```

## Examples

Shows how to ensure a row node contains the nodes we need to begin adding content to it.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Rows contain cells, containing paragraphs with typical elements such as runs, shapes, and even other tables.
// Our new row has none of these nodes, and we cannot add contents to it until it does.
Assert.That(row.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(0));

// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one cell with an empty paragraph.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### See Also

* class [Row](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
