---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: .NET için Aspose.Words
description: Belgelerde kolay filigran özelleştirmesi için Aspose.Words.WatermarkType enum'unu keşfedin. Çok yönlü filigran seçenekleriyle projelerinizi geliştirin!
type: docs
weight: 7540
url: /tr/net/aspose.words/watermarktype/
---
## WatermarkType enumeration

Filigran türünü belirtir.

```csharp
public enum WatermarkType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Text | `0` | Metnin filigran olarak kullanılacağını belirtir. |
| Image | `1` | Görüntünün filigran olarak kullanılacağını belirtir. |
| None | `2` | Filigranın ayarlanmadığını gösterir. |

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
