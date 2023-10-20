---
title: Watermark.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Watermark Remove yöntem. Filigranı kaldırır C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/watermark/remove/
---
## Watermark.Remove method

Filigranı kaldırır.

```csharp
public void Remove()
```

## Örnekler

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

* class [Watermark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
