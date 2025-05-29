---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: .NET için Aspose.Words
description: Şekillerinizdeki ham görüntü baytlarını gelişmiş görsel içerik için kolayca yönetmek ve düzenlemek amacıyla ImageData ImageBytes özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Şekilde depolanan görüntünün ham baytlarını alır veya ayarlar.

```csharp
public byte[] ImageBytes { get; set; }
```

## Notlar

Değeri ayarlamak`hükümsüz` veya boş bir dizi, resmi şekilden kaldıracaktır.

İade`hükümsüz` eğer resim belgede saklanmamışsa (örneğin bu durumda resim muhtemelen bağlantılıdır).

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
