---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words for .NET
description: ImageData ImageBytes mülk. Şekilde saklanan görüntünün ham baytlarını alır veya ayarlar C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Şekilde saklanan görüntünün ham baytlarını alır veya ayarlar.

```csharp
public byte[] ImageBytes { get; set; }
```

## Notlar

Değeri şu şekilde ayarlama:`hükümsüz` veya boş bir dizi, görüntüyü şekilden kaldıracaktır.

İadeler`hükümsüz` görüntü belgede saklanmıyorsa (örneğin, bu durumda görüntü muhtemelen bağlantılıdır).

## Örnekler

Bir şeklin ham görüntü verilerinden nasıl görüntü dosyası oluşturulacağını gösterir.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray(), ImageBytes özelliğinde saklanan diziyi döndürür.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Şeklin görüntü verilerini yerel dosya sistemindeki bir görüntü dosyasına kaydedin.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### Ayrıca bakınız

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
