---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: .NET için Aspose.Words
description: Belgelerinizdeki metin akışını kolayca kontrol etmek için Aspose.Words.DocumentDirection enum'unu keşfedin. Bu güçlü özellik ile okunabilirliği ve biçimlendirmeyi geliştirin!
type: docs
weight: 4030
url: /tr/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

Bir belgedeki metnin akış yönünü belirtmenize olanak tanır.

```csharp
public enum DocumentDirection
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| LeftToRight | `0` | Soldan sağa doğru. |
| RightToLeft | `1` | Sağdan sola doğru. |
| Auto | `2` | Yönü otomatik algıla. |

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

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
