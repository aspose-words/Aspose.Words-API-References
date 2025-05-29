---
title: SmartTag.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SmartTag NodeType, которое улучшает ваш контент с помощью динамических функций тегирования. Разблокируйте бесшовную интеграцию и увеличьте вовлеченность пользователей!
type: docs
weight: 30
url: /ru/net/aspose.words.markup/smarttag/nodetype/
---
## SmartTag.NodeType property

ВозвратSmartTag .

```csharp
public override NodeType NodeType { get; }
```

## Примеры

Показывает, как обойти дерево дочерних узлов составного узла.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Любой узел, который может содержать дочерние узлы, например сам документ, является составным.
    Assert.True(doc.IsComposite);

    // Вызываем рекурсивную функцию, которая пройдет и выведет все дочерние узлы составного узла.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Рекурсивно обходит дерево узлов, выводя тип каждого узла
/// с отступом, зависящим от глубины, а также от содержимого всех встроенных узлов.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Рекурсия в узел, если это составной узел. В противном случае, выводим его содержимое, если это встроенный узел.
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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [SmartTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
