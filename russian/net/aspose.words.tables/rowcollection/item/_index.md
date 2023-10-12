---
title: RowCollection.Item
second_title: Справочник по API Aspose.Words для .NET
description: RowCollection свойство. ПолучаетRow по данному индексу.
type: docs
weight: 10
url: /ru/net/aspose.words.tables/rowcollection/item/
---
## RowCollection indexer

Получает[`Row`](../../row/) по данному индексу.

```csharp
public Row this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс в коллекции. |

### Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний элемент и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицателен и его абсолютное значение превышает количество элементов в списке, возвращается нулевая ссылка.

### Примеры

Показывает, как перебрать все таблицы в документе и распечатать содержимое каждой ячейки.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Мы можем использовать метод ToArray для коллекции строк, чтобы клонировать ее в массив.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Мы можем использовать метод ToArray для коллекции ячеек, чтобы клонировать ее в массив.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

### Смотрите также

* class [Row](../../row/)
* class [RowCollection](../)
* пространство имен [Aspose.Words.Tables](../../rowcollection/)
* сборка [Aspose.Words](../../../)


