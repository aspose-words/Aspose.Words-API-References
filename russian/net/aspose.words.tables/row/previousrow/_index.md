---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: Aspose.Words для .NET
description: Воспользуйтесь свойством PreviousRow, чтобы легко извлечь предыдущий узел строки, что улучшит навигацию по данным и оптимизирует рабочий процесс кодирования.
type: docs
weight: 100
url: /ru/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Получает предыдущий[`Row`](../) узел.

```csharp
public Row PreviousRow { get; }
```

## Примечания

Метод можно использовать, когда вам нужен типизированный доступ к строкам таблицы. Если a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) узел найден в таблице вместо строки, он автоматически просматривается, чтобы получить строку, содержащуюся в.

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

* class [Row](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
