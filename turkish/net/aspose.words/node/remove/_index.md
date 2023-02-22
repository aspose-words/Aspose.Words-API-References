---
title: Node.Remove
second_title: Aspose.Words for .NET API Referansı
description: Node yöntem. Kendini üst öğeden kaldırır.
type: docs
weight: 150
url: /tr/net/aspose.words/node/remove/
---
## Node.Remove method

Kendini üst öğeden kaldırır.

```csharp
public void Remove()
```

### Örnekler

Bir belgeden görüntülü tüm şekillerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Belirli bir türdeki tüm alt düğümlerin bileşik düğümden nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Bir sonraki kardeş düğümü, bu düğümü sildikten sonra ona geçmek istersek bir değişken olarak kaydedin.
    Node nextNode = curNode.NextSibling;

    // Bir bölüm gövdesi Paragraf ve Tablo düğümleri içerebilir.
    // Düğüm bir Tablo ise, onu üst öğeden kaldırın.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

### Ayrıca bakınız

* class [Node](../)
* ad alanı [Aspose.Words](../../node/)
* toplantı [Aspose.Words](../../../)


