---
title: TableCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Получите доступ к элементам TableCollection без усилий, извлекая таблицы по определенным индексам. Упростите управление данными с помощью нашей интуитивной функции свойств!
type: docs
weight: 10
url: /ru/net/aspose.words.tables/tablecollection/item/
---
## TableCollection indexer

Извлекает[`Table`](../../table/) по данному индексу.

```csharp
public Table this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Указатель коллекции. |

## Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ с конца коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и т. д.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается пустая ссылка.

## Примеры

Показывает, как выполнить итерацию по всем таблицам в документе и распечатать содержимое каждой ячейки.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Мы можем использовать метод «ToArray» для коллекции строк, чтобы клонировать ее в массив.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Мы можем использовать метод «ToArray» для коллекции ячеек, чтобы клонировать ее в массив.
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

* class [Table](../../table/)
* class [TableCollection](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
