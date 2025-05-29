---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words для .NET
description: Оптимизируйте структуру ячеек с помощью метода EnsureMinimum, без усилий добавляйте абзац, если последний дочерний элемент не является таковым. Повысьте ясность вашего документа!
type: docs
weight: 160
url: /ru/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Если последний дочерний элемент не является абзацем, создает и добавляет один пустой абзац.

```csharp
public void EnsureMinimum()
```

## Примеры

Показывает, как обеспечить, чтобы узел ячейки содержал узлы, необходимые для начала добавления в него контента.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Ячейки могут содержать абзацы с типичными элементами, такими как строки, фигуры и даже другие таблицы.
// В нашей новой ячейке нет абзацев, и мы не можем добавлять в нее содержимое, такое как узлы трассы и формы, пока они не появятся.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// Вызов метода "EnsureMinimum" для ячейки гарантирует, что
// в ячейке есть как минимум один пустой абзац, в который мы затем можем добавить содержимое.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Смотрите также

* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
