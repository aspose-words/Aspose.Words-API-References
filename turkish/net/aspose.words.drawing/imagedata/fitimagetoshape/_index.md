---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: .NET için Aspose.Words
description: FitImageToShape yöntemiyle görsellerinizi optimize edin ve çarpıcı görsel sunumlar için Shape karelerinde mükemmel en boy oranı hizalamasını sağlayın.
type: docs
weight: 190
url: /tr/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

Görüntü verilerini Şekil çerçevesine uydurur, böylece görüntü verilerinin en boy oranı Şekil çerçevesinin en boy oranıyla eşleşir.

```csharp
public void FitImageToShape()
```

## Örnekler

Resim verisini Şekil çerçevesine uyacak şekilde sıcak gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir resim şekli ekleyin ve yönünü varsayılan durumunda bırakın.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### Ayrıca bakınız

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
