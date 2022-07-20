---
title: Layout
second_title: Aspose.Words for .NET API Referansı
description: Filigranın düzenini alır veya ayarlar. Varsayılan değerDiagonal .
type: docs
weight: 60
url: /tr/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

Filigranın düzenini alır veya ayarlar. Varsayılan değerDiagonal .

```csharp
public WatermarkLayout Layout { get; set; }
```

### Örnekler

Metin filigranının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Düz metin filigranı ekleyin.
doc.Watermark.SetText("Aspose Watermark");

// Metin biçimlendirmesini filigran olarak kullanarak düzenlemek istiyorsak,
// filigran oluştururken bir TextWatermarkOptions nesnesi ileterek bunu yapabiliriz.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Böyle bir belgeden bir filigranı kaldırabiliriz.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ayrıca bakınız

* enum [WatermarkLayout](../../watermarklayout)
* class [TextWatermarkOptions](../../textwatermarkoptions)
* ad alanı [Aspose.Words](../../textwatermarkoptions)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->