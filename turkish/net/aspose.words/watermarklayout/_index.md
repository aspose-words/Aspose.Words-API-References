---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: .NET için Aspose.Words
description: En iyi filigran konumlandırması için Aspose.Words.WatermarkLayout enumunu keşfedin. Hassas düzen kontrolü ve özelleştirmeyle belge tasarımınızı geliştirin.
type: docs
weight: 7530
url: /tr/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Filigranın, filigran merkezine göre düzenini tanımlar.

```csharp
public enum WatermarkLayout
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Horizontal | `0` | Yatay filigran düzeni. 0 derecelik dönüşe karşılık gelir. |
| Diagonal | `315` | Çapraz filigran düzeni. 315 derecelik dönüşe karşılık gelir. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
