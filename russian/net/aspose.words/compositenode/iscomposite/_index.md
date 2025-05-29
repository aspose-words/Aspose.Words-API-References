---
title: CompositeNode.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CompositeNode IsComposite. Легко проверяйте, поддерживает ли узел дочерние узлы для улучшенного управления структурой данных.
type: docs
weight: 40
url: /ru/net/aspose.words/compositenode/iscomposite/
---
## CompositeNode.IsComposite property

Возврат`истинный` так как этот узел может иметь дочерние узлы.

```csharp
public override bool IsComposite { get; }
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

* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
