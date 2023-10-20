---
title: GlossaryDocument.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words for .NET
description: GlossaryDocument NodeType mülk. Şunu döndürürGlossaryDocument değer C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.buildingblocks/glossarydocument/nodetype/
---
## GlossaryDocument.NodeType property

Şunu döndürür:GlossaryDocument değer.

```csharp
public override NodeType NodeType { get; }
```

## Örnekler

Bileşik bir düğümün alt düğüm ağacında nasıl gezinileceğini gösterir.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Belgenin kendisi gibi alt düğümleri içerebilen herhangi bir düğüm bileşiktir.
    Assert.True(doc.IsComposite);

    // Bileşik bir düğümün tüm alt düğümlerini tarayacak ve yazdıracak özyinelemeli işlevi çağırın.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Her düğümün türünü yazdırırken yinelemeli olarak bir düğüm ağacını geçer
/// tüm satır içi düğümlerin içeriğinin yanı sıra derinliğe bağlı olarak bir girinti ile.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Eğer düğüm bir bileşik düğümse, düğüme yineleme yapın. Aksi takdirde, satır içi düğüm ise içeriğini yazdırın.
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

### Ayrıca bakınız

* enum [NodeType](../../../aspose.words/nodetype/)
* class [GlossaryDocument](../)
* ad alanı [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* toplantı [Aspose.Words](../../../)
