---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: .NET için Aspose.Words
description: Alan kodlarındaki metni kolayca yönetmek için FindReplaceOptions IgnoreFieldCodes özelliğini keşfedin. Basit bir boolean ayarıyla görünürlüğü kontrol edin!
type: docs
weight: 70
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Alan kodları içindeki metni yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## Notlar

Bu seçenek yalnızca alan kodlarını etkiler ( arasındaki düğümleri yoksaymaz)FieldSeparator VeFieldEnd).

Tüm alanı yoksaymak için lütfen ilgili seçeneği kullanın[`IgnoreFields`](../ignorefields/).

## Örnekler

Alan kodları içindeki metnin nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Alan kodu içindeki metni dikkate almadan belgedeki 'T'yi değiştir.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
