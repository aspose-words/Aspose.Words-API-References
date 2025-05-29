---
title: TxtLoadOptions.DocumentDirection
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: .NET için Aspose.Words
description: Belge yönünü kolayca ayarlamak için TxtLoadOptions DocumentDirection özelliğini keşfedin. Varsayılan LeftToRight ayarıyla düzeninizi optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words.loading/txtloadoptions/documentdirection/
---
## TxtLoadOptions.DocumentDirection property

Bir belge yönünü alır veya ayarlar. Varsayılan değerLeftToRight .

```csharp
public DocumentDirection DocumentDirection { get; set; }
```

## Örnekler

Düz metin belge metin yönünün nasıl tespit edileceğini gösterir.

```csharp
// Bir belgenin oluşturucusuna geçirebileceğimiz bir "TxtLoadOptions" nesnesi oluşturun
// düz metin belgenin nasıl yükleneceğini değiştirmek için.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// "DocumentDirection" özelliğini "DocumentDirection.Auto" olarak ayarlayın, otomatik olarak algılar
// Aspose.Words'ün düz metinden yüklediği her metin paragrafının yönü.
// Her paragrafın "Bidi" özelliği onun yönünü saklayacaktır.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// İbranice metni sağdan sola olarak algıla.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// İngilizce metni sağdan sola doğru algıla.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Ayrıca bakınız

* enum [DocumentDirection](../../documentdirection/)
* class [TxtLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
