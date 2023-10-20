---
title: Node.NextSibling
linktitle: NextSibling
articleTitle: NextSibling
second_title: Aspose.Words для .NET
description: Node NextSibling свойство. Получает узел следующий сразу за этим узлом на С#.
type: docs
weight: 40
url: /ru/net/aspose.words/node/nextsibling/
---
## Node.NextSibling property

Получает узел, следующий сразу за этим узлом.

```csharp
public Node NextSibling { get; }
```

## Примечания

Если следующего узла нет,`нулевой` возвращается.

## Примеры

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

* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
