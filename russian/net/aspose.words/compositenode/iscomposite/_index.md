---
title: IsComposite
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает true так как этот узел может иметь дочерние узлы.
type: docs
weight: 50
url: /ru/net/aspose.words/compositenode/iscomposite/
---
## CompositeNode.IsComposite property

Возвращает true, так как этот узел может иметь дочерние узлы.

```csharp
public override bool IsComposite { get; }
```

### Примеры

Показывает, как пройти по дереву дочерних узлов составного узла.

```csharp
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Любой узел, который может содержать дочерние узлы, например сам документ, является составным.
    Assert.True(doc.IsComposite);

    // Вызываем рекурсивную функцию, которая будет проходить и печатать все дочерние узлы составного узла.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Рекурсивно обходит дерево узлов, печатая тип каждого узла
/// с отступом в зависимости от глубины, а также содержимого всех встроенных узлов.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Рекурсия к узлу, если это составной узел. В противном случае распечатайте его содержимое, если это встроенный узел.
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

* class [CompositeNode](../../compositenode)
* пространство имен [Aspose.Words](../../compositenode)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->