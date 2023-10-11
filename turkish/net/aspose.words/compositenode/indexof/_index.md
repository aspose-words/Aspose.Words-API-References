---
title: CompositeNode.IndexOf
second_title: Aspose.Words for .NET API Referansı
description: CompositeNode yöntem. Alt düğüm dizisinde belirtilen alt düğümün dizinini döndürür.
type: docs
weight: 140
url: /tr/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Alt düğüm dizisinde belirtilen alt düğümün dizinini döndürür.

```csharp
public int IndexOf(Node child)
```

### Notlar

Düğüm alt düğümlerde bulunamazsa -1 değerini döndürür.

### Örnekler

Belirli bir alt düğümün dizininin üst öğesinden nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// İlk bölümün gövdesindeki son paragrafın dizinini alın.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../compositenode/)
* toplantı [Aspose.Words](../../../)


