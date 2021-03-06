---
title: IndexOf
second_title: Aspose.Words for .NET API Referansı
description: Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür.
type: docs
weight: 130
url: /tr/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür.

```csharp
public int IndexOf(Node child)
```

### Notlar

Düğüm alt düğümlerde bulunmazsa -1 döndürür.

### Örnekler

Belirli bir alt düğümün dizininin üst öğesinden nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// İlk bölümün gövdesindeki son paragrafın dizinini alın.
Assert.AreEqual(24, body.ChildNodes.IndexOf(body.LastParagraph));
```

### Ayrıca bakınız

* class [Node](../../node)
* class [CompositeNode](../../compositenode)
* ad alanı [Aspose.Words](../../compositenode)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
