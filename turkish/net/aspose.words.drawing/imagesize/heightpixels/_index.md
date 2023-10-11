---
title: ImageSize.HeightPixels
second_title: Aspose.Words for .NET API Referansı
description: ImageSize mülk. Görüntünün yüksekliğini piksel cinsinden alır.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/imagesize/heightpixels/
---
## ImageSize.HeightPixels property

Görüntünün yüksekliğini piksel cinsinden alır.

```csharp
public int HeightPixels { get; }
```

### Örnekler

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
* ad alanı [Aspose.Words.Drawing](../../imagesize/)
* toplantı [Aspose.Words](../../../)


