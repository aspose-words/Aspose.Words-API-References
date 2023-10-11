---
title: ImageData.ToStream
second_title: Aspose.Words for .NET API Referansı
description: ImageData yöntem. Görüntü baytlarını içeren bir akış oluşturur ve döndürür.
type: docs
weight: 240
url: /tr/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Görüntü baytlarını içeren bir akış oluşturur ve döndürür.

```csharp
public Stream ToStream()
```

### Notlar

Görüntü baytları şekilde depolanıyorsa, birMemoryStream nesne.

Görüntü bağlantılıysa ve bir dosyada saklanıyorsa dosyayı açar ve birFileStream nesne.

Resim bağlantılıysa ve harici bir URL'de saklanıyorsa dosyayı indirir ve birMemoryStream nesne.

Akış nesnesini elden çıkarmak arayanın sorumluluğunda mıdır?

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


