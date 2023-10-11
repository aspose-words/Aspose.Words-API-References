---
title: HyphenationOptions.ConsecutiveHyphenLimit
second_title: Aspose.Words for .NET API Referansı
description: HyphenationOptions mülk. Kısa çizgilerle bitebilecek ardışık satırların maksimum sayısını alır veya ayarlar. Bu özelliğin varsayılan değeri 0. dir
type: docs
weight: 30
url: /tr/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

Kısa çizgilerle bitebilecek ardışık satırların maksimum sayısını alır veya ayarlar. Bu özelliğin varsayılan değeri 0. 'dir

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

### Notlar

Bu özelliğin değeri 0 olarak ayarlanırsa ardışık herhangi bir sayıda satır tire ile bitebilir.

Bu özelliğin, örneğin PDF gibi sabit sayfa formatlarına kaydederken etkisi yoktur.

### Örnekler

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
* ad alanı [Aspose.Words.Settings](../../hyphenationoptions/)
* toplantı [Aspose.Words](../../../)


