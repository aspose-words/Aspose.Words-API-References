---
title: ImageSaveOptions.TiffBinarizationMethod
linktitle: TiffBinarizationMethod
articleTitle: TiffBinarizationMethod
second_title: .NET için Aspose.Words
description: ImageSaveOptions için TiffBinarizationMethod özelliğini keşfedin. Görüntüleri Ccitt3 veya Ccitt4 sıkıştırmasıyla kolayca 1 bpp biçimine dönüştürün.
type: docs
weight: 170
url: /tr/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Görüntüleri 1 bpp formatına dönüştürürken kullanılan yöntemi alır veya ayarlar [`SaveFormat`](../saveformat/) dırTiff ve [`TiffCompression`](../tiffcompression/) eşittirCcitt3 veyaCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

## Notlar

Varsayılan değer:Threshold.

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

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
