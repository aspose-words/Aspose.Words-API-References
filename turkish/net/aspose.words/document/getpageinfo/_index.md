---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: .NET için Aspose.Words
description: Optimize edilmiş baskı ve gelişmiş belge yönetimi için temel sayfa boyutu, yönlendirme ve işleme ayrıntılarını almak üzere GetPageInfo yöntemini keşfedin.
type: docs
weight: 650
url: /tr/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

Yazdırma veya işleme için yararlı olabilecek bir sayfa hakkında sayfa boyutu, yönlendirme ve diğer bilgileri alır.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pageIndex | Int32 | 0 tabanlı sayfa indeksi. |

## Örnekler

Sayfanın renkli olup olmadığının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Belgenin ilk sayfasının renkli olmadığını kontrol edin.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Ayrıca bakınız

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
