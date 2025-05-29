---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: .NET için Aspose.Words
description: ImageData ToByteArray metoduyla herhangi bir resmi zahmetsizce bayt dizisine dönüştürün. Saklanan veya bağlantılı kaynaklardan resim baytlarına kolayca erişin!
type: docs
weight: 220
url: /tr/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Görüntünün depolanmış veya bağlantılı olup olmadığına bakılmaksızın herhangi bir görüntü için görüntü baytlarını döndürür.

```csharp
public byte[] ToByteArray()
```

## Notlar

Eğer resim bağlantılı ise her çağrıldığında resmi indirir.

## Örnekler

Bir şeklin ham görüntü verilerinden bir görüntü dosyasının nasıl oluşturulacağını gösterir.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() ImageBytes özelliğinde saklanan diziyi döndürür.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Şeklin görüntü verilerini yerel dosya sistemindeki bir görüntü dosyasına kaydet.
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
