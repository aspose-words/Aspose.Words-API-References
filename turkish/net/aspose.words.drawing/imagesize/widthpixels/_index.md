---
title: ImageSize.WidthPixels
linktitle: WidthPixels
articleTitle: WidthPixels
second_title: .NET için Aspose.Words
description: Görüntülerinizin piksel genişliğini kolayca almak, görüntü yönetiminizi ve optimizasyonunuzu geliştirmek için ImageSize WidthPixels özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing/imagesize/widthpixels/
---
## ImageSize.WidthPixels property

Görüntünün genişliğini piksel cinsinden alır.

```csharp
public int WidthPixels { get; }
```

## Örnekler

Bir şeklin içindeki görüntünün özelliklerinin nasıl okunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sistemimizden alınan bir görüntüyü içeren bir şekli belgeye ekleyin.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Şekil bir resim içeriyorsa, ImageData özelliği geçerli olacaktır,
// ve bir ImageSize nesnesi içerecektir.
ImageSize imageSize = shape.ImageData.ImageSize;

// ImageSize nesnesi, şekil içindeki görüntü hakkında salt okunur bilgileri içerir.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// Resmin gerilmesini önlemek için şeklin boyutunu resminin boyutuna göre belirleyebiliriz.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Ayrıca bakınız

* class [ImageSize](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
