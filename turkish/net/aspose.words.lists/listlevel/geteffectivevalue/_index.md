---
title: ListLevel.GetEffectiveValue
second_title: Aspose.Words for .NET API Referansı
description: ListLevel yöntem. Dizi gösterimini bildirir.ListLevelliste öğesinin belirtilen index nesnesi. Parametreler şunları belirtirNumberStyle ve aşağıdaki durumlarda kullanılan isteğe bağlı bir format string Custom belirtildi.
type: docs
weight: 190
url: /tr/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Dizi gösterimini bildirir.[`ListLevel`](../)liste öğesinin belirtilen index nesnesi. Parametreler şunları belirtir:[`NumberStyle`](../../../aspose.words/numberstyle/) ve aşağıdaki durumlarda kullanılan isteğe bağlı bir format string Custom belirtildi.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Liste öğesinin dizini (1 ile 32767 arasında olmalıdır). |
| numberStyle | NumberStyle | [`NumberStyle`](../../../aspose.words/numberstyle/) arasında[`ListLevel`](../) nesne. |
| customNumberStyleFormat | String | Aşağıdaki durumlarda kullanılan isteğe bağlı biçim dizesi:Custom belirtilir (örneğin "a, ç, ĝ, ..."). Diğer durumlarda bu parametre mutlaka`hükümsüz` veya boş. |

### Geri dönüş değeri

Dizi gösterimi[`ListLevel`](../) tarafından tanımlanan nesne*numberStyle* parametre ve *customNumberStyleFormat* parametresi, liste öğesi tarafından belirlenen konumda*index* parametre.

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* dır-dir`hükümsüz` veya boş olduğunda*numberStyle* özeldir.-veya- *customNumberStyleFormat* değil`hükümsüz` veya boş olduğunda*numberStyle* özel değildir.-or- *customNumberStyleFormat* geçersiz. |
| ArgumentOutOfRangeException | indeks aralık dışında. |

### Örnekler

Özel sayı stiline sahip bir listenin biçiminin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Liste öğesinin belirtilen indeksi için değer alabiliriz.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Ayrıca bakınız

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* ad alanı [Aspose.Words.Lists](../../listlevel/)
* toplantı [Aspose.Words](../../../)


