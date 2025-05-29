---
title: Watermark.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Markalaşma ve koruma için özelleştirilebilir filigranlarla tasarımınızı geliştirmek için Filigran Türü özelliğini keşfedin. Görsellerinizi bugün yükseltin!
type: docs
weight: 10
url: /tr/net/aspose.words/watermark/type/
---
## Watermark.Type property

Filigran türünü alır.

```csharp
public WatermarkType Type { get; }
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

* enum [WatermarkType](../../watermarktype/)
* class [Watermark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
