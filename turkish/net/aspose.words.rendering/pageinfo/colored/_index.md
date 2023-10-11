---
title: PageInfo.Colored
second_title: Aspose.Words for .NET API Referansı
description: PageInfo mülk. İadelerdoğru sayfa renkli içerik içeriyorsa.
type: docs
weight: 10
url: /tr/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

İadeler`doğru` sayfa renkli içerik içeriyorsa.

```csharp
public bool Colored { get; }
```

### Örnekler

Sayfanın renkli olup olmadığının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Belgenin ilk sayfasının renkli olmadığını kontrol edin.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Ayrıca bakınız

* class [PageInfo](../)
* ad alanı [Aspose.Words.Rendering](../../pageinfo/)
* toplantı [Aspose.Words](../../../)


