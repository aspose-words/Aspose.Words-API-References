---
title: CompositeNode.IsComposite
second_title: Справочник по API Aspose.Words для .NET
description: CompositeNode свойство. Возвращаетистинный поскольку этот узел может иметь дочерние узлы.
type: docs
weight: 40
url: /ru/net/aspose.words/compositenode/iscomposite/
---
## CompositeNode.IsComposite property

Возвращает`истинный` поскольку этот узел может иметь дочерние узлы.

```csharp
public override bool IsComposite { get; }
```

### Примеры

Показывает, как перемещаться по дереву дочерних узлов составного узла.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Любой узел, который может содержать дочерние узлы, например сам документ, является составным.
    Assert.True(doc.IsComposite);

    // Вызов рекурсивной функции, которая пройдёт и распечатает все дочерние узлы составного узла.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Рекурсивно обходит дерево узлов, печатая тип каждого узла
/// с отступом в зависимости от глубины, а также содержимого всех строчных узлов.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Рекурсия к узлу, если это составной узел. В противном случае выведите его содержимое, если это встроенный узел.
        if (childNode.IsComposite)
        {
            Console.WriteLine();
            TraverseAllNodes((CompositeNode)childNode, depth + 1);
        }
        else if (childNode is Inline)
        {
            Console.WriteLine($" - \"{childNode.GetText().Trim()}\"");
        }
        else
        {
            Console.WriteLine();
        }
    }
}
```

### Смотрите также

* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../compositenode/)
* сборка [Aspose.Words](../../../)


