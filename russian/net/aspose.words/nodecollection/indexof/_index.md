---
title: NodeCollection.IndexOf
second_title: Справочник по API Aspose.Words для .NET
description: NodeCollection метод. Возвращает индекс указанного узла начинающийся с нуля.
type: docs
weight: 70
url: /ru/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

Возвращает индекс указанного узла, начинающийся с нуля.

```csharp
public int IndexOf(Node node)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | Node | Узел, который необходимо найти. |

### Возвращаемое значение

Отсчитываемый от нуля индекс узла в коллекции, если он найден; в противном случае -1.

### Примечания

Этот метод выполняет линейный поиск; следовательно, среднее время выполнения пропорционально[`Count`](../count/).

### Примеры

Показывает, как получить индекс узла в коллекции.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.AreEqual(0, allTables.IndexOf(table));

Row row = table.Rows[2];

Assert.AreEqual(2, table.IndexOf(row));

Cell cell = row.LastCell;

Assert.AreEqual(4, row.IndexOf(cell));
```

### Смотрите также

* class [Node](../../node/)
* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../nodecollection/)
* сборка [Aspose.Words](../../../)


