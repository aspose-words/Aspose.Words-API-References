---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words для .NET
description: Откройте для себя свойство NextCell, чтобы легко получить доступ к следующему узлу Cell, улучшить управление данными и оптимизировать рабочий процесс.
type: docs
weight: 70
url: /ru/net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

Получает следующий[`Cell`](../) узел.

```csharp
public Cell NextCell { get; }
```

## Примечания

Метод можно использовать, когда вам необходимо иметь типизированный доступ к ячейкам[`Row`](../../row/) . Если a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) узел найден в строке, а не в ячейке, он автоматически проходится, чтобы получить ячейку, содержащуюся в.

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
