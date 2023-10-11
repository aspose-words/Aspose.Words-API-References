---
title: Node.NextPreOrder
second_title: Aspose.Words for .NET API Referansı
description: Node yöntem. Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır.
type: docs
weight: 130
url: /tr/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| rootNode | Node | Geçişin üst düğümü (sınırı). |

### Geri dönüş değeri

Ön sipariş sırasına göre sonraki düğüm. Ulaşıldığında boş*rootNode*.

### Örnekler

Ön sipariş geçiş algoritmasını kullanarak belgenin düğüm ağacında nasıl geçiş yapılacağını ve karşılaşılan herhangi bir şeklin görüntüyle nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

Assert.AreEqual(9, 
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));

Node curNode = doc;
while (curNode != null)
{
    Node nextNode = curNode.NextPreOrder(doc);

    if (curNode.PreviousPreOrder(doc) != null && nextNode != null)
        Assert.AreEqual(curNode, nextNode.PreviousPreOrder(doc));

    if (curNode.NodeType == NodeType.Shape && ((Shape)curNode).HasImage)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0,
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));
```

### Ayrıca bakınız

* class [Node](../)
* ad alanı [Aspose.Words](../../node/)
* toplantı [Aspose.Words](../../../)


