---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words для .NET
description: Откройте для себя свойство NextRow, чтобы легко получить доступ к следующему узлу строки, улучшив навигацию по данным и управление ими.
type: docs
weight: 70
url: /ru/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Получает следующий[`Row`](../) узел.

```csharp
public Row NextRow { get; }
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
