---
title: BookmarkEnd.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words для .NET
description: BookmarkEnd NodeType свойство. ВозвращаетBookmarkEnd  на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/bookmarkend/nodetype/
---
## BookmarkEnd.NodeType property

ВозвращаетBookmarkEnd .

```csharp
public override NodeType NodeType { get; }
```

## Примеры

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

* enum [NodeType](../../nodetype/)
* class [BookmarkEnd](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
