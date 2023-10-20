---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words for .NET
description: ImageSaveOptions ThresholdForFloydSteinbergDithering mülk. FloydSteinberg yöntemindeki ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. ne zamanImageBinarizationMethod dırdirFloydSteinbergDithering  C#'da.
type: docs
weight: 160
url: /tr/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Floyd-Steinberg yöntemindeki ikilileştirme hatasının değerini belirleyen eşiği alır veya ayarlar. ne zaman[`ImageBinarizationMethod`](../../imagebinarizationmethod/) dır-dirFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## Notlar

Varsayılan değer 128'dir.

## Örnekler

Bir TIFF görüntüsünü oluşturmak için Floyd-Steinberg yöntemini kullanırken TIFF ikilileştirme hatası eşiğinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi TIFF olarak kaydettiğimizde SaveOptions nesnesini iletebiliriz
// Aspose.Words'ün bu görüntüyü işlerken uygulayacağı renk taklidini ayarlayın.
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
