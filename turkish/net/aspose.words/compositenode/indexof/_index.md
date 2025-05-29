---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: .NET için Aspose.Words
description: CompositeNode IndexOf yönteminin dizideki belirtilen bir alt düğümün dizinini nasıl etkili bir şekilde bulduğunu keşfederek kodlama deneyiminizi geliştirin.
type: docs
weight: 140
url: /tr/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür.

```csharp
public int IndexOf(Node child)
```

## Notlar

Düğüm alt düğümlerde bulunmazsa -1 döndürür.

## Örnekler

Belirli bir alt düğümün dizininin üst düğümünden nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// İlk bölümün gövdesindeki son paragrafın dizinini al.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
