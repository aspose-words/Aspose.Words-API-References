---
title: Enum WatermarkLayout
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.WatermarkLayout Sıralama. Filigranın düzenini filigran merkezine göre tanımlar.
type: docs
weight: 6680
url: /tr/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Filigranın düzenini filigran merkezine göre tanımlar.

```csharp
public enum WatermarkLayout
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Horizontal | `0` | Yatay filigran düzeni. 0 derecelik dönüşe karşılık gelir. |
| Diagonal | `315` | Çapraz filigran düzeni. 315 derecelik dönüşe karşılık gelir. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


