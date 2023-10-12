---
title: ImageData.ToByteArray
second_title: Aspose.Words for .NET API Referansı
description: ImageData yöntem. Görüntünün depolanmış veya bağlı olmasına bakılmaksızın herhangi bir görüntü için görüntü baytlarını döndürür.
type: docs
weight: 220
url: /tr/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Görüntünün depolanmış veya bağlı olmasına bakılmaksızın herhangi bir görüntü için görüntü baytlarını döndürür.

```csharp
public byte[] ToByteArray()
```

### Notlar

Resim bağlantılıysa, her çağrıldığında resmi indirir.

### Örnekler

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
* ad alanı [Aspose.Words.Drawing](../../imagedata/)
* toplantı [Aspose.Words](../../../)


