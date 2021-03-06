---
title: GetEffectiveValue
second_title: Aspose.Words for .NET API Referansı
description: ListLevelaspose.words.lists/listlevel liste öğesinin belirtilen index nesnesi. Parametreler şunları belirtirNumberStyleaspose.words/numberstyle ve şu durumlarda kullanılan isteğe bağlı bir string biçimiCustom belirtildi.
type: docs
weight: 190
url: /tr/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

[`ListLevel`](../../listlevel) liste öğesinin belirtilen index nesnesi. Parametreler şunları belirtir:[`NumberStyle`](../../../aspose.words/numberstyle) ve şu durumlarda kullanılan isteğe bağlı bir string biçimiCustom belirtildi.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Liste öğesinin dizini (1 ile 32767 arasında olmalıdır). |
| numberStyle | NumberStyle | [`NumberStyle`](../../../aspose.words/numberstyle) arasında[`ListLevel`](../../listlevel) nesne. |
| customNumberStyleFormat | String | Şu durumlarda kullanılan isteğe bağlı biçim dizesi:Custom belirtilir (örn. "a, ç, ĝ, ..."). Diğer durumlarda bu parametre boş veya boş olmalıdır. |

### Geri dönüş değeri

[`ListLevel`](../../listlevel) index parametresi tarafından belirlenen konumda liste öğesinde numberStyle parametresi ve customNumberStyleFormat parametresi tarafından açıklanan nesne.

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | customNumberStyleFormat, numberStyle özel olduğunda boş veya boş.-veya- customNumberStyleFormat, numberStyle özel olmadığında boş veya boş değil.-veya- customNumberStyleFormat geçersiz. |
| ArgumentOutOfRangeException | dizin aralık dışında. |

### Örnekler

Özel sayı stiline sahip bir liste biçiminin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Liste öğesinin belirtilen dizini için değer alabiliriz.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Ayrıca bakınız

* enum [NumberStyle](../../../aspose.words/numberstyle)
* class [ListLevel](../../listlevel)
* ad alanı [Aspose.Words.Lists](../../listlevel)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
