---
title: Node.PreviousPreOrder
linktitle: PreviousPreOrder
articleTitle: PreviousPreOrder
second_title: Aspose.Words for .NET
description: Node PreviousPreOrder yöntem. Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır C#'da.
type: docs
weight: 140
url: /tr/net/aspose.words/node/previouspreorder/
---
## Node.PreviousPreOrder method

Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır.

```csharp
public Node PreviousPreOrder(Node rootNode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| rootNode | Node | Geçişin üst düğümü (sınırı). |

### Geri dönüş değeri

Ön sipariş sırasındaki önceki düğüm. Ulaşıldığında boş*rootNode*.

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
