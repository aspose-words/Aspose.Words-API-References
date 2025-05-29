---
title: TextWatermarkOptions Class
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: .NET için Aspose.Words
description: Özelleştirilebilir metin filigranları için Aspose.Words.TextWatermarkOptions'ı keşfedin. Belgelerinizi benzersiz, profesyonel markalama seçenekleriyle geliştirin!
type: docs
weight: 7290
url: /tr/net/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class

Metin içeren bir filigran eklerken belirtilebilecek seçenekleri içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Filigranla Çalışma](https://docs.aspose.com/words/net/working-with-watermark/) belgeleme makalesi.

```csharp
public class TextWatermarkOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [TextWatermarkOptions](textwatermarkoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Color](../../aspose.words/textwatermarkoptions/color/) { get; set; } | Yazı tipi rengini alır veya ayarlar. Varsayılan değerSilver . |
| [FontFamily](../../aspose.words/textwatermarkoptions/fontfamily/) { get; set; } | Yazı tipi aile adını alır veya ayarlar. Varsayılan değer "Calibri"dir. |
| [FontSize](../../aspose.words/textwatermarkoptions/fontsize/) { get; set; } | Bir yazı tipi boyutu alır veya ayarlar. Varsayılan değer 0'dır - auto. |
| [IsSemitrasparent](../../aspose.words/textwatermarkoptions/issemitrasparent/) { get; set; } | Filigranın opaklığından sorumlu olan bir Boole değeri alır veya ayarlar. Varsayılan değer`doğru` . |
| [Layout](../../aspose.words/textwatermarkoptions/layout/) { get; set; } | Filigranın düzenini alır veya ayarlar. Varsayılan değerDiagonal . |

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
