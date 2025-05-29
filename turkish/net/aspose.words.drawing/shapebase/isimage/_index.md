---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: .NET için Aspose.Words
description: ShapeBase'in IsImage özelliğiyle bir şeklin görüntü olup olmadığını keşfedin. Gelişmiş tasarım esnekliği ve işlevselliği için görüntü şekillerini kolayca tanımlayın.
type: docs
weight: 300
url: /tr/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

Geri Döndürür`doğru` eğer bu şekil bir görüntü şekliyse.

```csharp
public bool IsImage { get; }
```

## Örnekler

Bir akıştan gelen görselleri içeren bir HTML belgesinin temel URI kullanılarak nasıl açılacağını gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Yükleme sırasında temel klasörün URI'sini geçirin
    // böylece HTML belgesinde bağıl URI'leri olan tüm resimler bulunabilir.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Belgenin ilk şeklinin geçerli bir resim içerdiğini doğrulayın.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
