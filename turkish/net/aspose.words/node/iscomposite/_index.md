---
title: Node.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words for .NET
description: Node IsComposite mülk. İadelerdoğru bu düğüm başka düğümler içeriyorsa C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

İadeler`doğru` bu düğüm başka düğümler içeriyorsa.

```csharp
public virtual bool IsComposite { get; }
```

### Mülk değeri

Bu yöntem döndürür`YANLIŞ` gibi[`Node`](../) alt düğümlere sahip olamaz.

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

* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
