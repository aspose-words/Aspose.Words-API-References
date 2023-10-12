---
title: ITextShaperFactory.GetTextShaper
second_title: Aspose.Words for .NET API Referansı
description: ITextShaperFactory yöntem. Tarafından belirtilen yazı tipi için metin şekillendiricinin yeni örneğini döndürürfontPath VefaceIndex .
type: docs
weight: 10
url: /tr/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(string, int) {#gettextshaper_1}

Tarafından belirtilen yazı tipi için metin şekillendiricinin yeni örneğini döndürür*fontPath* Ve*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontPath | String | Yazı tipi dosyasının mutlak yolu. |
| faceIndex | Int32 | TrueType yazı tipi koleksiyonundaki yazı tipi yüzünün dizini, veya belirtilen yazı tipi dosyası TrueType yazı tipi koleksiyonu değilse 0. |

### Ayrıca bakınız

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* ad alanı [Aspose.Words.Shaping](../../itextshaperfactory/)
* toplantı [Aspose.Words](../../../)

---

## GetTextShaper(string, byte[], int) {#gettextshaper}

Şununla temsil edilen yazı tipi için metin şekillendiricinin yeni örneğini döndürür:*fontBlob* Ve*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontId | String | Sağlanan yazı tipiyle benzersiz şekilde ilişkilendirilebilecek benzersiz bir tanımlayıcı*fontBlob* . |
| fontBlob | Byte[] | Yazı tipi verilerini içeren bayt dizisi. |
| faceIndex | Int32 | TrueType yazı tipi koleksiyonundaki yazı tipi yüzünün dizini, veya eğer 0 ise*fontBlob* TrueType yazı tipi koleksiyonu değil. |

### Ayrıca bakınız

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* ad alanı [Aspose.Words.Shaping](../../itextshaperfactory/)
* toplantı [Aspose.Words](../../../)


