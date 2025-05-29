---
title: Node.GetAncestor
linktitle: GetAncestor
articleTitle: GetAncestor
second_title: Aspose.Words для .NET
description: Откройте для себя метод Node GetAncestor, позволяющий легко получить первого предка указанного типа объекта, что повышает эффективность и точность кодирования.
type: docs
weight: 110
url: /ru/net/aspose.words/node/getancestor/
---
## GetAncestor(*Type*) {#getancestor_1}

Получает первого предка указанного типа объекта.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | Type | Тип объекта предка, который необходимо извлечь. |

### Возвращаемое значение

Предок указанного типа или`нулевой` если предок данного типа не найден.

## Примечания

Тип предка совпадает, если он равен*ancestorType* или полученный из*ancestorType*.

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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## GetAncestor(*[NodeType](../../nodetype/)*) {#getancestor}

Получает первого предка указанного[`NodeType`](../../nodetype/) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | NodeType | Тип узла предка, который необходимо извлечь. |

### Возвращаемое значение

Предок указанного типа или`нулевой` если предок данного типа не найден.

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

* class [CompositeNode](../../compositenode/)
* enum [NodeType](../../nodetype/)
* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
