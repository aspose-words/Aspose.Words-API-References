---
title: Cell.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words для .NET
description: Откройте для себя таблицы ячеек. Легко получайте доступ к коллекции таблиц прямо в вашей ячейке для упрощения организации и улучшенного управления данными.
type: docs
weight: 120
url: /ru/net/aspose.words.tables/cell/tables/
---
## Cell.Tables property

Получает коллекцию таблиц, которые являются непосредственными дочерними элементами ячейки.

```csharp
public TableCollection Tables { get; }
```

## Примеры

Показывает, как определить, являются ли таблицы вложенными.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Выясняем, есть ли у ячеек таблицы другие дочерние таблицы.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Выясняем, вложена ли таблица в другую таблицу, и если да, то на какой глубине.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Вычисляет уровень вложенности таблицы в другие таблицы.
/// </summary>
/// <returns>
/// Целое число, указывающее глубину вложенности таблицы (количество узлов родительской таблицы).
/// </returns>
private static int GetNestedDepthOfTable(Table table)
{
    int depth = 0;
    Node parent = table.GetAncestor(table.NodeType);

    while (parent != null)
    {
        depth++;
        parent = parent.GetAncestor(typeof(Table));
    }

    return depth;
}

/// <summary>
/// Определяет, содержит ли таблица какие-либо непосредственные дочерние таблицы в своих ячейках.
/// Не выполняйте рекурсивный обход этих таблиц для проверки наличия дополнительных таблиц.
/// </summary>
/// <returns>
/// Возвращает true, если хотя бы одна дочерняя ячейка содержит таблицу.
/// Возвращает false, если ни одна ячейка в таблице не содержит таблицу.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows)
    {
        foreach (Cell Cell in row.Cells)
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### Смотрите также

* class [TableCollection](../../tablecollection/)
* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
