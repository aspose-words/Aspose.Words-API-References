---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: .NET için Aspose.Words
description: Sayfanızın canlı renkli içeriklere sahip olup olmadığını PageInfo Colored özelliğiyle keşfedin. Kullanıcı etkileşimini artırın ve görsel çekiciliği geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Geri Döndürür`doğru` eğer sayfa renkli içerik içeriyorsa.

```csharp
public bool Colored { get; }
```

## Örnekler

Sayfanın renkli olup olmadığının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Belgenin ilk sayfasının renkli olmadığını kontrol edin.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Ayrıca bakınız

* class [PageInfo](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
