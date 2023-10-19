---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ImageData sınıf. Bir şekle ilişkin görüntüyü tanımlar C#'da.
type: docs
weight: 1060
url: /tr/net/aspose.words.drawing/imagedata/
---
## ImageData class

Bir şekle ilişkin görüntüyü tanımlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Görsellerle Çalışmak](https://docs.aspose.com/words/net/working-with-images/) dokümantasyon makalesi.

```csharp
public class ImageData
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Bir görüntünün siyah beyaz görüntülenip görüntülenmeyeceğini belirler. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Görüntünün kenarlıklarının koleksiyonunu alır. Kenarlıklar yalnızca satır içi resimlerde etkilidir. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Resmin parlaklığını alır veya ayarlar. Bu özelliğin değeri 0,0 (en soluk) ila 1,0 (en parlak) arasında bir sayı olmalıdır. |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Şeffaf olarak değerlendirilecek görüntünün renk değerini tanımlar. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Belirtilen resmin kontrastını alır veya ayarlar. Bu özellik için value , 0,0 (en az kontrast) ila 1,0 (en büyük kontrast) arasında bir sayı olmalıdır. |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Alt taraftan resim kaldırma oranını tanımlar. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Resmin sol taraftan kaldırılma oranını tanımlar. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Resmin sağ taraftan kaldırılma oranını tanımlar. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Resmin üst taraftan kaldırılma oranını tanımlar. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Bir resmin gri tonlamalı modda görüntülenip görüntülenmeyeceğini belirler. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | İadeler`doğru` şeklin görüntü baytları varsa veya bir görüntüye bağlantı veriyorsa. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Şekilde saklanan görüntünün ham baytlarını alır veya ayarlar. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Görüntü boyutu ve çözünürlüğü hakkında bilgi alır. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Görüntünün türünü alır. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | İadeler`doğru` görüntü şekle bağlıysa (ne zaman[`SourceFullName`](./sourcefullname/) belirtildi). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | İadeler`doğru` resim bağlantılıysa ve belgede saklanmıyorsa. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Bağlı görüntünün kaynak dosyasının yolunu ve adını alır veya ayarlar. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Bir görüntünün başlığını tanımlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | Görüntüyü belirtilen akışa kaydeder. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | Görüntüyü bir dosyaya kaydeder. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | Şeklin görüntüleyeceği görüntüyü ayarlar. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | Şeklin görüntüleyeceği görüntüyü ayarlar. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | Şeklin görüntüleyeceği görüntüyü ayarlar. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Görüntünün depolanmış veya bağlı olmasına bakılmaksızın herhangi bir görüntü için görüntü baytlarını döndürür. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Şekilde saklanan görüntüyü bir dosya olarak alır.Image nesne. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Görüntü baytlarını içeren bir akış oluşturur ve döndürür. |

## Notlar

Kullan[`ImageData`](../shape/imagedata/) bir şeklin içindeki görüntüye erişmek ve onu değiştirmek için kullanılan özellik. `ImageData` doğrudan sınıf.

Bir görüntü bir şeklin içinde saklanabilir, harici bir dosyaya bağlanabilir veya her ikisi de yapılabilir (bağlanabilir ve belgede saklanabilir).

Görüntünün şeklin içinde mi yoksa bağlantılı mı saklandığına bakılmaksızın, active görüntüsüne her zaman şunu kullanarak erişebilirsiniz:[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) veya[`Save`](./save/) method. Görüntü şeklin içinde saklanıyorsa, ona doğrudan[`ImageBytes`](./imagebytes/) mülk.

Bir resmi bir şeklin içinde saklamak için şunu kullanın:[`SetImage`](./setimage/) yöntem. Bir görüntüyü bir şekle bağlamak için[`SourceFullName`](./sourcefullname/) mülk.

## Örnekler

Bir belgeden görüntülerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgedeki şekillerin koleksiyonunu alın,
// ve resim içeren her şeklin resim verilerini dosya olarak yerel dosya sistemine kaydedin.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Şekillerin görüntü verileri birçok olası görüntü formatındaki görüntüleri içerebilir.
        // Her görsel için formatına göre otomatik olarak bir dosya uzantısı belirleyebiliriz.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Bağlantılı bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Aşağıda, bir şekli görüntüleyebilmesi için bir şekle uygulamanın iki yolu verilmiştir.
// 1 - Resmi içerecek şekli ayarlayın.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Şekilde sakladığımız her görsel belgemizin boyutunu artıracaktır.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Yerel dosya sistemindeki bir görüntü dosyasına bağlanacak şekli ayarlayın.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Resimlere bağlantı verilmesi yerden tasarruf sağlar ve belgenin daha küçük olmasını sağlar.
// Ancak belge görüntüyü yalnızca doğru şekilde görüntüleyebilir
// görüntü dosyası, şeklin "SourceFullName" özelliğinin işaret ettiği konumda mevcut.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
