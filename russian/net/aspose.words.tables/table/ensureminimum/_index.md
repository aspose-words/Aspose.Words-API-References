---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words для .NET
description: Table EnsureMinimum метод. Если в таблице нет строк создается и добавляется однаRow  на С#.
type: docs
weight: 400
url: /ru/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Если в таблице нет строк, создается и добавляется одна[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Примеры

Показывает, как убедиться, что узел таблицы содержит узлы, необходимые для добавления содержимого.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Таблицы содержат строки, содержащие ячейки, которые могут содержать абзацы
// с типичными элементами, такими как прогоны, фигуры и даже другие таблицы.
// В нашей новой таблице нет ни одного из этих узлов, и мы не можем добавлять в нее содержимое, пока он не появится.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Вызов метода EnsureMinimum для таблицы гарантирует, что
// в таблице есть хотя бы одна строка и одна ячейка с пустым абзацем.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
