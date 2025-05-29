---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: .NET için Aspose.Words
description: Belgelerinize filigranları kolayca eklemek ve özelleştirmek, profesyonelliği ve markalamayı geliştirmek için Aspose.Words.Watermark sınıfını keşfedin.
type: docs
weight: 7520
url: /tr/net/aspose.words/watermark/
---
## Watermark class

Belge filigranıyla çalışmak için sınıfı temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Filigranla Çalışma](https://docs.aspose.com/words/net/working-with-watermark/) belgeleme makalesi.

```csharp
public sealed class Watermark
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | Filigran türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | Filigranı kaldırır. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | Belgeye Resim filigranı ekler. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Belgeye Resim filigranı ekler. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Belgeye Resim filigranı ekler. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Belgeye Resim filigranı ekler. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | Belgeye Metin filigranı ekler. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Belgeye Metin filigranı ekler. |

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
