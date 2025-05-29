---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: Node Clone yöntemi ile düğümleri zahmetsizce çoğaltın. Geliştirme sürecinizi geliştirin ve proje verimliliğini bugünden itibaren artırın!
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
| isCloneChildren | Boolean | Belirtilen düğümün altındaki alt ağacı yinelemeli olarak klonlamak için True; yalnızca düğümün kendisini klonlamak için false. |

### Geri dönüş değeri

Klonlanmış düğüm.

## Notlar

Bu yöntem düğümler için bir kopyalama oluşturucusu olarak hizmet eder. Klonlanan düğümün üst öğesi yoktur, ancak orijinal düğümle aynı belgeye aittir.

Bu yöntem her zaman düğümün derin bir kopyasını gerçekleştirir.*isCloneChildren* parameter tüm alt düğümlerin de kopyalanıp kopyalanmayacağını belirtir.

## Örnekler

Bileşik bir düğümün nasıl klonlanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Aşağıda bir bileşik düğümü klonlamanın iki yolu bulunmaktadır.
// 1 - Bir düğümün klonunu oluştur ve ayrıca onun her bir alt düğümünün bir klonunu oluştur.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Herhangi bir çocuğu olmadan sadece kendi başına bir düğümün klonunu oluştur.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Ayrıca bakınız

* class [Node](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
