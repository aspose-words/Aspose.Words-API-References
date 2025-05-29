---
title: TextWatermarkOptions.Layout
linktitle: Layout
articleTitle: Layout
second_title: .NET için Aspose.Words
description: Filigranınızın görünümünü özelleştirmek için TextWatermarkOptions Düzen özelliğini keşfedin. Gelişmiş görseller için bunu kolayca Çapraz veya tercih ettiğiniz düzene ayarlayın.
type: docs
weight: 60
url: /tr/net/aspose.words/textwatermarkoptions/layout/
---
## TextWatermarkOptions.Layout property

Filigranın düzenini alır veya ayarlar. Varsayılan değerDiagonal .

```csharp
public WatermarkLayout Layout { get; set; }
```

## Örnekler

Metin filigranının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Düz metin filigranı ekleyin.
doc.Watermark.SetText("Aspose Watermark");

// Eğer metin biçimlendirmesini filigran olarak kullanarak düzenlemek istersek,
// filigranı oluştururken TextWatermarkOptions nesnesini geçirerek bunu yapabiliriz.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Bir belgeden filigranı şu şekilde kaldırabiliriz.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ayrıca bakınız

* enum [WatermarkLayout](../../watermarklayout/)
* class [TextWatermarkOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
