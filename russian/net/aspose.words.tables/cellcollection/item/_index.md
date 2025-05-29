---
title: CellCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Получите доступ к определенным ячейкам без усилий с помощью свойства CellCollection Item. Извлеките любую ячейку по индексу для оптимизированного управления данными и повышения производительности.
type: docs
weight: 10
url: /ru/net/aspose.words.tables/cellcollection/item/
---
## CellCollection indexer

Извлекает[`Cell`](../../cell/) по данному индексу.

```csharp
public Cell this[int index] { get; }
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

* class [Cell](../../cell/)
* class [CellCollection](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
