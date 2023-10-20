---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.ImageBinarizationMethod Sıralama. Görüntüyü ikili hale getirmek için kullanılan yöntemi belirtir C#'da.
type: docs
weight: 5200
url: /tr/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Görüntüyü ikili hale getirmek için kullanılan yöntemi belirtir.

```csharp
public enum ImageBinarizationMethod
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Threshold | `0` | Eşik yöntemini belirtir. |
| FloydSteinbergDithering | `1` | Floyd-Steinberg hata dağıtma yöntemini kullanarak renk taklidini belirtir. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
