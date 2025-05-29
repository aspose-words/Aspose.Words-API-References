---
title: Node.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: Düğümleri ana düğümlerinden zahmetsizce ayırmak, kodunuzun verimliliğini ve yapısını artırmak için Node Remove yöntemini keşfedin.
type: docs
weight: 150
url: /tr/net/aspose.words/node/remove/
---
## Node.Remove method

Kendini ana öğeden kaldırır.

```csharp
public void Remove()
```

## Örnekler

Bir belgeden resimli tüm şekillerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Belirli bir türdeki tüm alt düğümlerin bileşik bir düğümden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Bu düğümü sildikten sonra ona geçmek istersek, bir sonraki kardeş düğümü bir değişken olarak kaydet.
    Node nextNode = curNode.NextSibling;

    // Bir bölüm gövdesi Paragraf ve Tablo düğümlerini içerebilir.
    // Eğer düğüm bir Tablo ise, onu ana düğümden kaldır.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

### Ayrıca bakınız

* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
