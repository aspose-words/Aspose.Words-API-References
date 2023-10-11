---
title: TextWatermarkOptions.Layout
second_title: Aspose.Words for .NET API Referansı
description: TextWatermarkOptions mülk. Filigranın düzenini alır veya ayarlar. Varsayılan değerDiagonal .
type: docs
weight: 60
url: /tr/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

Filigranın düzenini alır veya ayarlar. Varsayılan değer:Diagonal .

```csharp
public WatermarkLayout Layout { get; set; }
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

* enum [WatermarkLayout](../../watermarklayout/)
* class [TextWatermarkOptions](../)
* ad alanı [Aspose.Words](../../textwatermarkoptions/)
* toplantı [Aspose.Words](../../../)


