---
title: Story.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words for .NET
description: Discover Story Tables: a curated collection of tables directly linked to your story, enhancing organization and engagement effortlessly.
type: docs
weight: 50
url: /net/aspose.words/story/tables/
---
## Story.Tables property

Gets a collection of tables that are immediate children of the story.

```csharp
public TableCollection Tables { get; }
```

## Examples

Shows how to remove the first and last rows of all tables in a document.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

### See Also

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [Story](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
