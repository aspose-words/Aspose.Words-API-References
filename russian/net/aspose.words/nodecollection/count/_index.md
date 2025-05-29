---
title: NodeCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: Откройте для себя свойство NodeCollection Count, чтобы легко получить доступ к общему количеству узлов в вашей коллекции, улучшая управление данными и эффективность.
type: docs
weight: 10
url: /ru/net/aspose.words/nodecollection/count/
---
## NodeCollection.Count property

Получает количество узлов в коллекции.

```csharp
public int Count { get; }
```

## Примеры

Показывает, как проходить по коллекции дочерних узлов составного узла.

```csharp
Document doc = new Document();

// Добавьте две трассы и одну форму в качестве дочерних узлов в первый абзац этого документа.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Обратите внимание, что «CustomNodeId» не сохраняется в выходном файле и существует только в течение срока службы узла.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Проходим по коллекции непосредственных дочерних элементов абзаца,
// и распечатать любые найденные нами фрагменты или формы.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

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

* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
