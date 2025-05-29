---
title: ImageSize.VerticalResolution
linktitle: VerticalResolution
articleTitle: VerticalResolution
second_title: .NET için Aspose.Words
description: Dikey DPI çözünürlüğüne kolayca erişmek, görüntü kalitenizi ve performansınızı artırmak için ImageSize VerticalResolution özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/imagesize/verticalresolution/
---
## ImageSize.VerticalResolution property

Dikey çözünürlüğü DPI olarak alır.

```csharp
public double VerticalResolution { get; }
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
