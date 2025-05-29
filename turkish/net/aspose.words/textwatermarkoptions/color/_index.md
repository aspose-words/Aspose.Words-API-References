---
title: TextWatermarkOptions.Color
linktitle: Color
articleTitle: Color
second_title: .NET için Aspose.Words
description: Görünürlüğü artırmak için Color özelliğiyle TextWatermarkOptions'ınızı özelleştirin. Kişiselleştirilmiş bir dokunuş için tercih ettiğiniz yazı tipi rengini ayarlayın. Varsayılan, Gümüş.
type: docs
weight: 20
url: /tr/net/aspose.words/textwatermarkoptions/color/
---
## TextWatermarkOptions.Color property

Yazı tipi rengini alır veya ayarlar. Varsayılan değerSilver .

```csharp
public Color Color { get; set; }
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

* class [TextWatermarkOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
