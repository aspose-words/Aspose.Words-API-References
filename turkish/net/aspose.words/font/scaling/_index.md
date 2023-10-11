---
title: Font.Scaling
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Karakter genişliği ölçeklendirmesini yüzde cinsinden alır veya ayarlar.
type: docs
weight: 310
url: /tr/net/aspose.words/font/scaling/
---
## Font.Scaling property

Karakter genişliği ölçeklendirmesini yüzde cinsinden alır veya ayarlar.

```csharp
public int Scaling { get; set; }
```

### Örnekler

Karakterler için yatay ölçeklendirmenin ve aralığın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metnin tamamını ekleyin ve karakter genişliğini %150'ye yükseltin.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Metnin tamamını ekleyin ve her karakterin arasına 1 punto ekstra yatay boşluk ekleyin.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Metnin tamamını ekleyin ve karakterleri 1 punto kadar birbirine yaklaştırın.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


