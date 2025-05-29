---
title: Node.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: .NET için Aspose.Words
description: Node IsComposite özelliğini keşfedin. Bir düğümün diğer düğümleri tutup tutamayacağını kolayca belirleyerek veri yapınızın yönetimini ve esnekliğini artırın.
type: docs
weight: 30
url: /tr/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

Geri Döndürür`doğru` eğer bu düğüm diğer düğümleri içerebiliyorsa.

```csharp
public virtual bool IsComposite { get; }
```

### Mülk değeri

Bu yöntem şunu döndürür:`YANLIŞ` gibi[`Node`](../) alt düğümlere sahip olamaz.

## Örnekler

Bir bileşik düğümün alt düğüm ağacında nasıl gezinileceğini gösterir.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Belgenin kendisi gibi alt düğümleri içerebilen herhangi bir düğüm bileşiktir.
    Assert.True(doc.IsComposite);

    // Bileşik bir düğümün tüm alt düğümlerini tarayacak ve yazdıracak olan yinelemeli işlevi çağır.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Her düğümün türünü yazdırırken düğüm ağacını yinelemeli olarak dolaşır
/// Derinliğe ve tüm satır içi düğümlerin içeriğine bağlı olarak girintili.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Bileşik bir düğüm ise düğüme tekrarla. Aksi takdirde, satır içi bir düğüm ise içeriğini yazdır.
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
