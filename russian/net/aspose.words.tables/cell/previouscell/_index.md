---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: Aspose.Words для .NET
description: Cell PreviousCell свойство. Получает предыдущееCell узел на С#.
type: docs
weight: 110
url: /ru/net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

Получает предыдущее[`Cell`](../) узел.

```csharp
public Cell PreviousCell { get; }
```

## Примечания

Этот метод можно использовать, когда вам необходимо иметь типизированный доступ к ячейкам[`Row`](../../row/) . Если a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) узел найден в строке, а не в ячейке, он автоматически проходится, чтобы получить ячейку, содержащуюся внутри.

## Примеры

Показывает, как перебрать все ячейки таблицы.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Перебираем все ячейки таблицы.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Смотрите также

* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
