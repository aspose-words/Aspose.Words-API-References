---
title: Node.Clone
second_title: Aspose.Words for .NET API Referansı
description: Node yöntem. Düğümün bir kopyasını oluşturur.
type: docs
weight: 100
url: /tr/net/aspose.words/node/clone/
---
## Node.Clone method

Düğümün bir kopyasını oluşturur.

```csharp
public Node Clone(bool isCloneChildren)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| isCloneChildren | Boolean | Belirtilen düğümün altındaki alt ağacı yinelemeli olarak klonlamak için True; Yalnızca düğümün kendisini klonlamak için false. |

### Geri dönüş değeri

Klonlanmış düğüm.

### Notlar

Bu yöntem, düğümler için bir kopya oluşturucu görevi görür. Klonlanan düğümün üst öğesi yoktur ancak orijinal düğümle aynı belgeye aittir.

Bu yöntem her zaman düğümün derin bir kopyasını gerçekleştirir.*isCloneChildren* parametre tüm alt düğümlerin de kopyalanıp kopyalanmayacağını belirtir.

### Örnekler

Bileşik düğümün nasıl kopyalanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Aşağıda bileşik bir düğümü klonlamanın iki yolu verilmiştir.
// 1 - Bir düğümün klonunu oluşturun ve aynı zamanda onun alt düğümlerinin her birinin bir kopyasını oluşturun.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Hiçbir çocuk olmadan tek başına bir düğümün klonunu oluşturun.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Ayrıca bakınız

* class [Node](../)
* ad alanı [Aspose.Words](../../node/)
* toplantı [Aspose.Words](../../../)


