---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words для .NET
description: Откройте для себя метод Table EnsureMinimum, легко создавайте и добавляйте строки, когда ваша таблица пуста, для бесперебойного управления данными.
type: docs
weight: 420
url: /ru/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Если в таблице нет строк, создает и добавляет одну[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Примеры

Показывает, как обеспечить, чтобы узел таблицы содержал узлы, необходимые для добавления контента.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Таблицы содержат строки, которые содержат ячейки, которые могут содержать абзацы
// с типичными элементами, такими как ряды, фигуры и даже другие таблицы.
// В нашей новой таблице нет ни одного из этих узлов, и мы не можем добавлять в нее содержимое, пока их нет.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Вызов метода "EnsureMinimum" для таблицы гарантирует, что
// в таблице есть как минимум одна строка и одна ячейка с пустым абзацем.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
