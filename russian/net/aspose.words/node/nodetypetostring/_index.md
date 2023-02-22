---
title: Node.NodeTypeToString
second_title: Справочник по API Aspose.Words для .NET
description: Node метод. Вспомогательный метод который преобразует значение перечисления типа узла в удобную для пользователя строку.
type: docs
weight: 170
url: /ru/net/aspose.words/node/nodetypetostring/
---
## Node.NodeTypeToString method

Вспомогательный метод, который преобразует значение перечисления типа узла в удобную для пользователя строку.

```csharp
public static string NodeTypeToString(NodeType nodeType)
```

### Примеры

Показывает, как использовать свойство NextSibling узла для перечисления его непосредственных дочерних элементов.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

for (Node node = doc.FirstSection.Body.FirstChild; node != null; node = node.NextSibling)
{
    Console.WriteLine();
    Console.WriteLine($"Node type: {Node.NodeTypeToString(node.NodeType)}");

    string contents = node.GetText().Trim();
    Console.WriteLine(contents == string.Empty ? "This node contains no text" : $"Contents: \"{node.GetText().Trim()}\"");
}
```

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

* enum [NodeType](../../nodetype/)
* class [Node](../)
* пространство имен [Aspose.Words](../../node/)
* сборка [Aspose.Words](../../../)


