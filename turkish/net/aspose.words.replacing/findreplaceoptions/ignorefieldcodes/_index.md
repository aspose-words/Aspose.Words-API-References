---
title: FindReplaceOptions.IgnoreFieldCodes
second_title: Aspose.Words for .NET API Referansı
description: FindReplaceOptions mülk. Alan kodları içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değeryanlış .
type: docs
weight: 70
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Alan kodları içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer`yanlış` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

### Notlar

Bu seçenek yalnızca alan kodlarını etkiler ( arasındaki düğümleri yok saymaz)FieldSeparator veFieldEnd).

Tüm alanı yok saymak için lütfen ilgili seçeneği kullanın[`IgnoreFields`](../ignorefields/).

### Örnekler

Alan kodlarının içindeki metnin nasıl yok sayılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Alan kodunun içindeki metni yok sayarak belgede 'T'yi değiştirin.
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


