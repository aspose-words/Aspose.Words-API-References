---
title: RtfLoadOptions.RtfLoadOptions
second_title: Aspose.Words for .NET API Referansı
description: RtfLoadOptions inşaatçı. Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```csharp
public RtfLoadOptions()
```

### Örnekler

Bir RTF belgesi yüklenirken UTF-8 karakterlerinin nasıl algılanacağını gösterir.

```csharp
// Bir RTF belgesini yükleme şeklimizi değiştirmek için bir "RtfLoadOptions" nesnesi oluşturun.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Belgenin ISO 8859-1 karakter setini kullandığını varsaymak için "RecognizeUtf8Text" özelliğini "false" olarak ayarlayın
// ve belgedeki her karakteri yükler.
// Metinde oluşabilecek değişken uzunluktaki karakterleri ayrıştırmak için "RecognizeUtf8Text" özelliğini "true" olarak ayarlayın.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Ayrıca bakınız

* class [RtfLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../rtfloadoptions/)
* toplantı [Aspose.Words](../../../)


