---
title: ImageSize.HorizontalResolution
linktitle: HorizontalResolution
articleTitle: HorizontalResolution
second_title: Aspose.Words for .NET
description: ImageSize HorizontalResolution mülk. Yatay çözünürlüğü DPI cinsinden alır C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/imagesize/horizontalresolution/
---
## ImageSize.HorizontalResolution property

Yatay çözünürlüğü DPI cinsinden alır.

```csharp
public double HorizontalResolution { get; }
```

## Örnekler

Bir şekildeki görüntünün özelliklerinin nasıl okunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yerel dosya sistemimizden alınmış bir resmi içeren belgeye bir şekil ekleyin.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Şekil bir resim içeriyorsa ImageData özelliği geçerli olacaktır,
// ve bir ImageSize nesnesi içerecektir.
ImageSize imageSize = shape.ImageData.ImageSize; 

// ImageSize nesnesi, şeklin içindeki görüntü hakkında salt okunur bilgiler içerir.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// Resmin esnemesini önlemek için şeklin boyutunu resmin boyutuna göre ayarlayabiliriz.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Ayrıca bakınız

* class [ImageSize](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
