---
title: TextWatermarkOptions.IsSemitrasparent
linktitle: IsSemitrasparent
articleTitle: IsSemitrasparent
second_title: .NET için Aspose.Words
description: TextWatermarkOptions IsSemitransparent özelliğini keşfedin; filigran opaklığını kolayca kontrol edin. Tasarımlarınızı özelleştirilebilir şeffaflık ayarlarıyla geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

Filigranın opaklığından sorumlu olan bir Boole değeri alır veya ayarlar. Varsayılan değer`doğru` .

```csharp
public bool IsSemitrasparent { get; set; }
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
