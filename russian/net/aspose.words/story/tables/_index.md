---
title: Story.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words для .NET
description: Откройте для себя Story Tables — тщательно подобранную коллекцию таблиц, напрямую связанных с вашей историей, которая легко улучшает организацию и вовлеченность.
type: docs
weight: 50
url: /ru/net/aspose.words/story/tables/
---
## Story.Tables property

Получает коллекцию таблиц, которые являются непосредственными дочерними элементами истории.

```csharp
public TableCollection Tables { get; }
```

## Примеры

Показывает, как удалить первую и последнюю строки всех таблиц в документе.

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

### Смотрите также

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [Story](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
