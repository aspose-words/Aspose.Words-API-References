---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words for .NET
description: Discover the Table LastRow property to easily access the final Row node in your table, enhancing data management and efficiency.
type: docs
weight: 180
url: /net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Returns the last [`Row`](../../row/) node in the table.

```csharp
public Row LastRow { get; }
```

## Examples

Shows how to remove the first and last rows of all tables in a document.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.That(tables[0].Rows.Count, Is.EqualTo(5));
Assert.That(tables[1].Rows.Count, Is.EqualTo(4));

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.That(tables[0].Rows.Count, Is.EqualTo(3));
Assert.That(tables[1].Rows.Count, Is.EqualTo(2));
```

### See Also

* class [Row](../../row/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
