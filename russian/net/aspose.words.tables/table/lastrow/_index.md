---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table LastRow, чтобы легко получить доступ к последнему узлу строки в таблице, что улучшает управление данными и эффективность.
type: docs
weight: 180
url: /ru/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Возвращает последний[`Row`](../../row/) узел в таблице.

```csharp
public Row LastRow { get; }
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

* class [Row](../../row/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
