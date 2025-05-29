---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: .NET için Aspose.Words
description: Aspose.Words.Drawing.ImageData sınıfını keşfedin—resimleri şekillerde tanımlama ve yönetme çözümünüz. Belge tasarımınızı zahmetsizce geliştirin!
type: docs
weight: 1390
url: /tr/net/aspose.words.drawing/imagedata/
---
## ImageData class

Bir şekil için bir görüntü tanımlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Görüntülerle Çalışma](https://docs.aspose.com/words/net/working-with-images/) belgeleme makalesi.

```csharp
public class ImageData
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Bir görüntünün siyah beyaz olarak gösterilip gösterilmeyeceğini belirler. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Görüntünün kenarlık koleksiyonunu alır. Kenarlıklar yalnızca satır içi görüntüler için etkilidir. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Resmin parlaklığını alır veya ayarlar. Bu özelliğin değeri 0,0 (en sönük) ile 1,0 (en parlak) arasında bir sayı olmalıdır. |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Şeffaf olarak ele alınacak görüntünün renk değerini tanımlar. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Belirtilen resim için kontrastı alır veya ayarlar. Bu özellik için value 0,0 (en az kontrast) ile 1,0 (en büyük kontrast) arasında bir sayı olmalıdır. |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Alt taraftan resim kaldırma oranını tanımlar. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Resmin sol taraftan kaldırılma oranını tanımlar. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Sağ taraftan resim kaldırma oranını tanımlar. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Resmin üst taraftan kaldırılma oranını tanımlar. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Bir resmin gri tonlamalı modda görüntülenip görüntülenmeyeceğini belirler. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Geri Döndürür`doğru` eğer şeklin görüntü baytları varsa veya bir görüntüye bağlantı veriyorsa. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Şekilde depolanan görüntünün ham baytlarını alır veya ayarlar. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Görüntü boyutu ve çözünürlüğü hakkında bilgi alır. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Görüntünün türünü alır. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Geri Döndürür`doğru` eğer görüntü şekle bağlıysa (ne zaman[`SourceFullName`](./sourcefullname/) belirtilmiştir). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Geri Döndürür`doğru` eğer görüntü bağlantılıysa ve belgede saklanmıyorsa. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Bağlantılı görüntü için kaynak dosyasının yolunu ve adını alır veya ayarlar. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Bir görüntünün başlığını tanımlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() | Görüntü verilerini Şekil çerçevesine uydurur, böylece görüntü verilerinin en boy oranı Şekil çerçevesinin en boy oranıyla eşleşir. |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | Görüntüyü belirtilen akışa kaydeder. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | Görüntüyü bir dosyaya kaydeder. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | Şeklin görüntülediği görüntüyü ayarlar. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | Şeklin görüntülediği görüntüyü ayarlar. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | Şeklin görüntülediği görüntüyü ayarlar. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Görüntünün depolanmış veya bağlantılı olup olmadığına bakılmaksızın herhangi bir görüntü için görüntü baytlarını döndürür. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Şekilde depolanan görüntüyü birImage nesne. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Görüntü baytlarını içeren bir akış oluşturur ve döndürür. |

## Notlar

Kullanın[`ImageData`](../shape/imagedata/)Bir şeklin içindeki görüntüye erişmek ve onu değiştirmek için özellik. Örnekleri oluşturmazsınız`ImageData` sınıfa doğrudan.

Bir resim bir şeklin içerisinde saklanabilir, harici bir dosyaya bağlanabilir veya her ikisi de yapılabilir (bağlantı verilebilir ve belgede saklanabilir).

Görüntünün şeklin içinde depolanmış veya bağlantılı olup olmadığına bakılmaksızın, actual görüntüsüne her zaman şu komutu kullanarak erişebilirsiniz:[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) veya[`Save`](./save/) methods. Görüntü şeklin içinde saklanıyorsa, doğrudan şu yöntemi kullanarak da erişebilirsiniz:[`ImageBytes`](./imagebytes/) mülk.

Bir şeklin içinde bir görüntüyü depolamak için şunu kullanın:[`SetImage`](./setimage/) yöntem. Bir görüntüyü bir şekle bağlamak için,[`SourceFullName`](./sourcefullname/) mülk.

## Örnekler

Bir belgeden resimlerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Şekil koleksiyonunu belgeden al,
// ve her şeklin görüntü verisini, görüntü içeren bir dosya olarak yerel dosya sistemine kaydeder.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Şekillerin görüntü verileri birçok olası görüntü formatındaki görüntüleri içerebilir.
        // Her bir resim için, formatına bağlı olarak otomatik olarak bir dosya uzantısı belirleyebiliriz.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Bağlantılı bir resmin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Aşağıda bir şeklin görüntülenebilmesi için bir resmin üzerine uygulanmasının iki yolu bulunmaktadır.
// 1 - Şekli resmi içerecek şekilde ayarlayın.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Şekilde depoladığımız her resim, belgemizin boyutunu artıracaktır.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Şekli yerel dosya sistemindeki bir resim dosyasına bağlanacak şekilde ayarlayın.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Resimlere bağlantı vermek yerden tasarruf sağlayacak ve daha küçük bir belgeyle sonuçlanacaktır.
// Ancak belge, yalnızca aşağıdaki durumlarda görüntüyü doğru şekilde görüntüleyebilir:
// resim dosyası şeklin "SourceFullName" özelliğinin işaret ettiği konumda mevcuttur.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
