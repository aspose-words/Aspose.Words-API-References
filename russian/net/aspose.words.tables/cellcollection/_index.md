---
title: CellCollection Class
linktitle: CellCollection
articleTitle: CellCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.Tables.CellCollection сорт. Обеспечивает типизированный доступ к коллекцииCell узлы на С#.
type: docs
weight: 6250
url: /ru/net/aspose.words.tables/cellcollection/
---
## CellCollection class

Обеспечивает типизированный доступ к коллекции[`Cell`](../cell/) узлы.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) статья документации.

```csharp
public class CellCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words.tables/cellcollection/item/) { get; } | Получает[`Cell`](../cell/) по данному индексу. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Определяет, находится ли узел в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Обеспечивает простую итерацию стиля foreach по коллекции узлов. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Возвращает индекс указанного узла, начинающийся с нуля. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Вставляет узел в коллекцию по указанному индексу. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [ToArray](../../aspose.words.tables/cellcollection/toarray/#toarray_1)() | Копирует все ячейки из коллекции в новый массив ячеек. (2 methods) |

## Примеры

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

* class [NodeCollection](../../aspose.words/nodecollection/)
* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)
