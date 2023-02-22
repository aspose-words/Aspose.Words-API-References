---
title: Font.Spacing
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Karakterler arasındaki boşluğu nokta olarak döndürür veya ayarlar .
type: docs
weight: 380
url: /tr/net/aspose.words/font/spacing/
---
## Font.Spacing property

Karakterler arasındaki boşluğu (nokta olarak) döndürür veya ayarlar .

```csharp
public double Spacing { get; set; }
```

### Örnekler

Karakterler için yatay ölçekleme ve aralığın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metin akışı ekleyin ve karakter genişliğini %150'ye yükseltin.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Metin dizisi ekleyin ve her karakter arasına 1pt fazladan yatay boşluk ekleyin.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Bir dizi metin ekleyin ve karakterleri 1 punto ile birbirine yaklaştırın.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


