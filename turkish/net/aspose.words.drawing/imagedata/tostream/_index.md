---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: .NET için Aspose.Words
description: ImageData ToStream yöntemini keşfedin; sorunsuz veri işleme ve gelişmiş uygulama performansı için görüntüleri bayt akışlarına verimli bir şekilde dönüştürün.
type: docs
weight: 240
url: /tr/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Görüntü baytlarını içeren bir akış oluşturur ve döndürür.

```csharp
public Stream ToStream()
```

## Notlar

Resim baytları şekil içinde depolanırsa, bir tane oluşturur ve döndürürMemoryStream nesne.

Resim bağlantılıysa ve bir dosyada saklanıyorsa, dosyayı açar ve birFileStream nesne.

Resim bağlantılıysa ve harici bir URL'de saklanıyorsa, dosyayı indirir ve birMemoryStream nesne.

Akış nesnesini elden çıkarmak çağıranın sorumluluğunda mıdır?

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
