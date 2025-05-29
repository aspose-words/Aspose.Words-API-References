---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: .NET için Aspose.Words
description: Görüntülerinizi Floyd-Steinberg Dithering için ImageSaveOptions Eşiği ile optimize edin. Görüntü işlemede çarpıcı sonuçlar için binarizasyon hatasını kontrol edin.
type: docs
weight: 160
url: /tr/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Floyd-Steinberg yöntemindeki ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. ne zaman[`ImageBinarizationMethod`](../../imagebinarizationmethod/) dırFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## Notlar

Varsayılan değer 128'dir.

## Örnekler

Floyd-Steinberg yöntemi kullanılarak bir TIFF görüntüsünün oluşturulması sırasında TIFF ikilileştirme hatası eşiğinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi TIFF olarak kaydettiğimizde, SaveOptions nesnesini geçirebiliriz
// Aspose.Words'ün bu resmi işlerken uygulayacağı titreşimi ayarlayın.
// "ThresholdForFloydSteinbergDithering" özelliğinin varsayılan değeri 128'dir.
// Daha yüksek değerler daha koyu görüntüler üretme eğilimindedir.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
