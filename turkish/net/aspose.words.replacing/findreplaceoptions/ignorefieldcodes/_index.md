---
title: FindReplaceOptions.IgnoreFieldCodes
second_title: Aspose.Words for .NET API Referansı
description: FindReplaceOptions mülk. Alan kodları içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ .
type: docs
weight: 70
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Alan kodları içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

### Notlar

Bu seçenek yalnızca alan kodlarını etkiler ( arasındaki düğümleri göz ardı etmez)FieldSeparator VeFieldEnd).

Alanın tamamını yoksaymak için lütfen ilgili seçeneği kullanın[`IgnoreFields`](../ignorefields/).

### Örnekler

Alan kodları içindeki metnin nasıl yok sayılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Alan kodu içindeki metni yok sayarak belgedeki 'T'yi değiştirin veya değiştirmeyin.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../findreplaceoptions/)
* toplantı [Aspose.Words](../../../)


