---
title: Story.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words for .NET
description: Discover Story Tables, a curated collection of tables directly linked to your story, enhancing organization and engagement effortlessly.
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

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [Story](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
