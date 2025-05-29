---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: .NET için Aspose.Words
description: RtfLoadOptions RecognizeUtf8Text özelliğinin içe aktarma sırasında UTF-8 karakterlerini nasıl koruduğunu, böylece doğru metin gösterimini ve sorunsuz entegrasyonu nasıl sağladığını keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

Ayarlandığında`doğru` , UTF8 karakterlerini algılamaya çalışacak, bunlar içe aktarma sırasında korunacaktır.

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## Notlar

Varsayılan değer`YANLIŞ`.

## Örnekler

Bir RTF belgesi yüklenirken UTF-8 karakterlerinin nasıl algılanacağını gösterir.

```csharp
// Bir RTF belgesini nasıl yükleyeceğimizi değiştirmek için bir "RtfLoadOptions" nesnesi oluşturun.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Belgenin ISO 8859-1 karakter setini kullandığını varsaymak için "RecognizeUtf8Text" özelliğini "false" olarak ayarlayın
// ve belgedeki her karakteri yükler.
// Metinde bulunabilecek değişken uzunluktaki karakterleri ayrıştırmak için "RecognizeUtf8Text" özelliğini "true" olarak ayarlayın.
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
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
