---
title: Row.EnsureMinimum
second_title: Справочник по API Aspose.Words для .NET
description: Row метод. ЕслиRow не имеет ячеек создает и добавляет однуCell .
type: docs
weight: 150
url: /ru/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Если[`Row`](../) не имеет ячеек, создает и добавляет одну[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

### Примеры

Показывает, как убедиться, что узел строки содержит узлы, которые нам нужны, чтобы начать добавлять к нему содержимое.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Строки содержат ячейки, содержащие абзацы с типичными элементами, такими как прогоны, фигуры и даже другие таблицы.
// В нашей новой строке нет ни одного из этих узлов, и мы не можем добавлять в нее содержимое, пока он не появится.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Вызов метода EnsureMinimum для таблицы гарантирует, что
// в таблице есть хотя бы одна ячейка с пустым абзацем.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Смотрите также

* class [Row](../)
* пространство имен [Aspose.Words.Tables](../../row/)
* сборка [Aspose.Words](../../../)


