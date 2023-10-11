---
title: TableCollection.ToArray
second_title: Справочник по API Aspose.Words для .NET
description: TableCollection метод. Копирует все таблицы из коллекции в новый массив таблиц.
type: docs
weight: 20
url: /ru/net/aspose.words.tables/tablecollection/toarray/
---
## TableCollection.ToArray method

Копирует все таблицы из коллекции в новый массив таблиц.

```csharp
public Table[] ToArray()
```

### Возвращаемое значение

Массив таблиц.

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

* class [Table](../../table/)
* class [TableCollection](../)
* пространство имен [Aspose.Words.Tables](../../tablecollection/)
* сборка [Aspose.Words](../../../)


