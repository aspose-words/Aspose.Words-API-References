---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: .NET için Aspose.Words
description: Belirli yazı tipi ihtiyaçlarınız için özel bir metin şekillendirici oluşturmak ve metin oluşturma deneyiminizi geliştirmek için ITextShaperFactory GetTextShaper yöntemini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

Belirtilen yazı tipi için yeni bir metin şekillendirici örneği döndürür*fontPath* Ve*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontPath | String | Yazı tipi dosyasına giden kesin yol. |
| faceIndex | Int32 | TrueType yazı tipi koleksiyonundaki yazı tipi yüzünün dizini, veya belirtilen yazı tipi dosyası TrueType yazı tipi koleksiyonu değilse 0. |

### Ayrıca bakınız

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* ad alanı [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* toplantı [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

Yazı tipi için metin şekillendiricinin yeni örneğini döndürür*fontBlob* Ve*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontId | String | Sağlanan yazı tipiyle benzersiz bir şekilde ilişkilendirilebilen benzersiz bir tanımlayıcı*fontBlob* . |
| fontBlob | Byte[] | Yazı tipi verilerinin bulunduğu bayt dizisi. |
| faceIndex | Int32 | TrueType yazı tipi koleksiyonundaki yazı tipi yüzünün dizini, veya 0*fontBlob* TrueType yazı tipi koleksiyonu değildir. |

### Ayrıca bakınız

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* ad alanı [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* toplantı [Aspose.Words](../../../)
