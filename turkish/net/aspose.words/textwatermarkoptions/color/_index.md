---
title: TextWatermarkOptions.Color
second_title: Aspose.Words for .NET API Referansı
description: TextWatermarkOptions mülk. Yazı tipi rengini alır veya ayarlar. Varsayılan değerSilver .
type: docs
weight: 20
url: /tr/net/aspose.words/textwatermarkoptions/color/
---
## TextWatermarkOptions.Color property

Yazı tipi rengini alır veya ayarlar. Varsayılan değer:Silver .

```csharp
public Color Color { get; set; }
```

### Örnekler

Metin filigranının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Düz metin filigranı ekleyin.
doc.Watermark.SetText("Aspose Watermark");

// Metin formatını filigran olarak kullanarak düzenlemek istersek,
// filigranı oluştururken bir TextWatermarkOptions nesnesini ileterek bunu yapabiliriz.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Bunun gibi bir belgeden filigranı kaldırabiliriz.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ayrıca bakınız

* class [TextWatermarkOptions](../)
* ad alanı [Aspose.Words](../../textwatermarkoptions/)
* toplantı [Aspose.Words](../../../)


