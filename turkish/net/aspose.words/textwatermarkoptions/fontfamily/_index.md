---
title: TextWatermarkOptions.FontFamily
linktitle: FontFamily
articleTitle: FontFamily
second_title: .NET için Aspose.Words
description: Tasarımlarınızı geliştirmek için TextWatermarkOptions'ınızı FontFamily özelliğiyle özelleştirin. Varsayılan Calibri'dir; markanıza uyan bir stil seçin!
type: docs
weight: 30
url: /tr/net/aspose.words/textwatermarkoptions/fontfamily/
---
## TextWatermarkOptions.FontFamily property

Yazı tipi aile adını alır veya ayarlar. Varsayılan değer "Calibri"dir.

```csharp
public string FontFamily { get; set; }
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
