---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: .NET için Aspose.Words
description: Karakter aralığını noktalar halinde kolayca ayarlamak için Font Aralığı özelliğini keşfedin. Hassas tipografik kontrolle okunabilirliği ve tasarımı geliştirin.
type: docs
weight: 390
url: /tr/net/aspose.words/font/spacing/
---
## Font.Spacing property

Karakterler arasındaki boşluğu (nokta cinsinden) döndürür veya ayarlar.

```csharp
public double Spacing { get; set; }
```

## Örnekler

Karakterler için yatay ölçeklendirme ve aralıkların nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metnin tamamını ekle ve karakter genişliğini %150'ye çıkar.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Metnin tamamını ekleyin ve her karakter arasına 1pt ekstra yatay boşluk ekleyin.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Metnin bir bölümünü ekle ve karakterleri birbirine 1pt yakınlaştır.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
