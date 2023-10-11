---
title: ImageSaveOptions.TiffBinarizationMethod
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. Görüntüleri 1 bpp format ye dönüştürürken kullanılan yöntemi alır veya ayarlar.SaveFormat dırdirTiff ve TiffCompression eşittirCcitt3 veyaCcitt4 .
type: docs
weight: 170
url: /tr/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Görüntüleri 1 bpp format 'ye dönüştürürken kullanılan yöntemi alır veya ayarlar.[`SaveFormat`](../saveformat/) dır-dirTiff ve [`TiffCompression`](../tiffcompression/) eşittirCcitt3 veyaCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

### Notlar

Varsayılan değer:Threshold.

### Örnekler

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

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


