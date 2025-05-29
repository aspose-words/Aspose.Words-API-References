---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: .NET için Aspose.Words
description: Liste öğelerinin dize gösterimlerini kolayca almak için ListLevel GetEffectiveValue yöntemini keşfedin. NumberStyle ve biçimlendirme seçenekleriyle özelleştirin!
type: docs
weight: 190
url: /tr/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Dize gösterimini bildirir[`ListLevel`](../)Liste öğesinin belirtilen index için nesne. Parametreler şunu belirtir:[`NumberStyle`](../../../aspose.words/numberstyle/) ve isteğe bağlı bir biçim string kullanıldığındaCustom belirtildi.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Liste öğesinin indeksi (1 ile 32767 aralığında olmalıdır). |
| numberStyle | NumberStyle | [`NumberStyle`](../../../aspose.words/numberstyle/) of'un[`ListLevel`](../) nesne. |
| customNumberStyleFormat | String | İsteğe bağlı biçim dizesi,Custom (örneğin "a, ç, ĝ, ...") belirtilir. Diğer durumlarda, bu parametrenin`hükümsüz` veya boş. |

### Geri dönüş değeri

Dize gösterimi[`ListLevel`](../) nesne, tarafından tanımlanan*numberStyle* parametre ve *customNumberStyleFormat* parametre, liste öğesinde, belirtilen konumda*index* parametre.

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* dır`hükümsüz` veya boş olduğunda*numberStyle* özeldir.-veya- *customNumberStyleFormat* değil`hükümsüz` veya boş olduğunda*numberStyle* özel değil.-veya- *customNumberStyleFormat* geçersizdir. |
| ArgumentOutOfRangeException | endeks aralık dışında. |

## Örnekler

Özel sayı stiline sahip bir listenin biçiminin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Liste öğesinin belirtilen indeksine ait değeri alabiliriz.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Ayrıca bakınız

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
