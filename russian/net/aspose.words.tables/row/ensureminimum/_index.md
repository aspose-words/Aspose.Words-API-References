---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words для .NET
description: Откройте для себя метод Row EnsureMinimum, с легкостью создавайте и добавляйте ячейки, если их нет, улучшая управление структурой данных.
type: docs
weight: 150
url: /ru/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Если[`Row`](../) не имеет ячеек, создает и добавляет одну[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

## Примеры

Показывает, как обеспечить, чтобы узел строки содержал узлы, необходимые для начала добавления в него контента.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Строки содержат ячейки, содержащие абзацы с типичными элементами, такими как строки, фигуры и даже другие таблицы.
// В нашей новой строке нет ни одного из этих узлов, и мы не можем добавлять в нее содержимое, пока они не появятся.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Вызов метода "EnsureMinimum" для таблицы гарантирует, что
// в таблице есть хотя бы одна ячейка с пустым абзацем.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Смотрите также

* class [Row](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
