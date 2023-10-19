---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words for .NET
description: TxtLoadOptions DocumentDirection mülk. Belge yönünü alır veya ayarlar. Varsayılan değerLeftToRight  C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Belge yönünü alır veya ayarlar. Varsayılan değer:LeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Örnekler

Düz metin belgesinin metin yönünün nasıl algılanacağını gösterir.

```csharp
// Bir belgenin yapıcısına iletebileceğimiz bir "TxtLoadOptions" nesnesi oluşturun
// düz metin belgesini yükleme şeklimizi değiştirmek için.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// "DocumentDirection" özelliğini "DocumentDirection.Auto" olarak ayarlayın, otomatik olarak algılar
// Aspose.Words'ün düz metinden yüklediği metnin her paragrafının yönü.
// Her paragrafın "Bidi" özelliği yönünü saklayacak.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// İbranice metni sağdan sola olarak algıla.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// İngilizce metni sağdan sola olarak algıla.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Ayrıca bakınız

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
