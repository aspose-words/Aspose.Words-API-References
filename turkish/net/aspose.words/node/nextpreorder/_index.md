---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: .NET için Aspose.Words
description: Verimli ağaç geçişi için Node NextPreOrder yöntemini keşfedin. Ön sipariş algoritmasını etkili bir şekilde kullanarak bir sonraki düğümü nasıl alacağınızı öğrenin!
type: docs
weight: 130
url: /tr/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır.

```csharp
public Node NextPreOrder(Node rootNode)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| rootNode | Node | Gezinmenin en üst düğümü (sınırı). |

### Geri dönüş değeri

Ön sipariş sırasındaki bir sonraki düğüm. Ulaşılırsa boş*rootNode*.

## Örnekler

Ön sipariş gezinme algoritmasını kullanarak belgenin düğüm ağacında nasıl gezinileceğini ve bir görüntüyle karşılaşılan herhangi bir şeklin nasıl silineceğini gösterir.

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
