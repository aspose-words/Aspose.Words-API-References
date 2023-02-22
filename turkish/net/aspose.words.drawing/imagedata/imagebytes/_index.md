---
title: ImageData.ImageBytes
second_title: Aspose.Words for .NET API Referansı
description: ImageData mülk. Şekilde saklanan görüntünün ham baytlarını alır veya ayarlar.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Şekilde saklanan görüntünün ham baytlarını alır veya ayarlar.

```csharp
public byte[] ImageBytes { get; set; }
```

### Notlar

Değerin ayarlanması`hükümsüz` veya boş bir dizi, görüntüyü şekilden kaldıracaktır.

İadeler`hükümsüz` resim belgede saklanmıyorsa (örneğin, bu durumda resim muhtemelen bağlantılıdır).

### Örnekler

Bir şeklin ham görüntü verilerinden bir görüntü dosyasının nasıl oluşturulacağını gösterir.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray(), ImageBytes özelliğinde depolanan diziyi döndürür.
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
* ad alanı [Aspose.Words.Drawing](../../imagedata/)
* toplantı [Aspose.Words](../../../)


