---
title: Row.PreviousRow
second_title: Справочник по API Aspose.Words для .NET
description: Row свойство. Получает предыдущееRow узел.
type: docs
weight: 100
url: /ru/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Получает предыдущее[`Row`](../) узел.

```csharp
public Row PreviousRow { get; }
```

### Примечания

Этот метод можно использовать, когда вам необходимо иметь типизированный доступ к строкам таблицы. Если a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)узел найден в таблице, а не в строке, он автоматически просматривается для получения строки, содержащейся внутри.

### Примеры

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
* пространство имен [Aspose.Words.Tables](../../row/)
* сборка [Aspose.Words](../../../)


