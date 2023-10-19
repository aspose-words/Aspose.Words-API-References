---
title: Node.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words for .NET
description: Node NodeType mülk. Bu düğümün türünü alır C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words/node/nodetype/
---
## Node.NodeType property

Bu düğümün türünü alır.

```csharp
public abstract NodeType NodeType { get; }
```

## Örnekler

Bir düğümün NextSibling özelliğinin, doğrudan alt öğeleri aracılığıyla numaralandırmak için nasıl kullanılacağını gösterir.

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

Belirli bir türdeki tüm alt düğümlerin bileşik bir düğümden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Bu düğümü sildikten sonra ona geçmek istersek diye bir sonraki kardeş düğümü değişken olarak kaydedin.
    Node nextNode = curNode.NextSibling;

    // Bir bölüm gövdesi Paragraf ve Tablo düğümleri içerebilir.
    // Düğüm bir Tablo ise onu ebeveynden kaldırın.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

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

* enum [NodeType](../../nodetype/)
* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
