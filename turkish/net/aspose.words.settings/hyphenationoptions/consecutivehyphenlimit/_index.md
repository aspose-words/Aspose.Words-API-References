---
title: HyphenationOptions.ConsecutiveHyphenLimit
linktitle: ConsecutiveHyphenLimit
articleTitle: ConsecutiveHyphenLimit
second_title: .NET için Aspose.Words
description: HyphenationOptions'daki ConsecutiveHyphenLimit özelliğini keşfedin. Metninizde tire kullanımını kontrol ederek daha iyi okunabilirlik ve biçimlendirme sağlayın. Varsayılan, 0.
type: docs
weight: 30
url: /tr/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

Tire ile bitebilecek ardışık satırların maksimum sayısını alır veya ayarlar. Bu özelliğin varsayılan değeri 0'dır.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

## Notlar

Bu özelliğin değeri 0 olarak ayarlanırsa, herhangi bir sayıda ardışık satır tire ile bitebilir.

Özelliğin, PDF gibi sabit sayfa biçimlerine kaydedildiğinde bir etkisi yoktur.

## Örnekler

Otomatik tirelemenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Ayrıca bakınız

* class [HyphenationOptions](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
