---
title: ImageData
second_title: Aspose.Words for .NET API Referansı
description: Bir şekil için bir resim tanımlar.
type: docs
weight: 930
url: /tr/net/aspose.words.drawing/imagedata/
---
## ImageData class

Bir şekil için bir resim tanımlar.

```csharp
public class ImageData
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel) { get; set; } | Bir görüntünün siyah beyaz gösterilip gösterilmeyeceğini belirler. |
| [Borders](../../aspose.words.drawing/imagedata/borders) { get; } | Resmin kenarlıklarının koleksiyonunu alır. Kenarlıklar yalnızca satır içi resimler için etkilidir. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness) { get; set; } | Resmin parlaklığını alır veya ayarlar. Bu özelliğin değeri 0.0 (en karanlık) ile 1.0 (en parlak) arasında bir sayı olmalıdır. |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey) { get; set; } | Saydam olarak değerlendirilecek görüntünün renk değerini tanımlar. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast) { get; set; } | Belirtilen resim için kontrastı alır veya ayarlar. Bu özellik için değer , 0,0 (en az karşıtlık) ile 1,0 (en büyük karşıtlık) arasında bir sayı olmalıdır. |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom) { get; set; } | Alt taraftan resmin kaldırılma oranını tanımlar. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft) { get; set; } | Sol taraftan resmin kaldırılma oranını tanımlar. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright) { get; set; } | Sağ taraftan resmin kaldırılma oranını tanımlar. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop) { get; set; } | Üst taraftan resmin kaldırılma oranını tanımlar. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale) { get; set; } | Bir resmin gri tonlama modunda gösterilip gösterilmeyeceğini belirler. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage) { get; } | Şekilde görüntü baytları varsa veya bir görüntüye bağlanırsa true değerini döndürür. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes) { get; set; } | Şekilde saklanan görüntünün ham baytlarını alır veya ayarlar. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize) { get; } | Görüntü boyutu ve çözünürlüğü hakkında bilgi alır. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype) { get; } | Resmin türünü alır. |
| [IsLink](../../aspose.words.drawing/imagedata/islink) { get; } | Görüntü şekle bağlıysa true döndürür (ne zaman[`SourceFullName`](./sourcefullname) belirtilir). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly) { get; } | Resim bağlantılıysa ve belgede saklanmıyorsa true değerini döndürür. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname) { get; set; } | Bağlantılı görüntü için kaynak dosyanın yolunu ve adını alır veya ayarlar. |
| [Title](../../aspose.words.drawing/imagedata/title) { get; set; } | Bir görüntünün başlığını tanımlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save#save)(Stream) | Resmi belirtilen akışa kaydeder. |
| [Save](../../aspose.words.drawing/imagedata/save#save_1)(string) | Resmi bir dosyaya kaydeder. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage#setimage)(Image) | Şeklin gösterdiği görüntüyü ayarlar. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage#setimage_1)(Stream) | Şeklin gösterdiği görüntüyü ayarlar. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage#setimage_2)(string) | Şeklin gösterdiği görüntüyü ayarlar. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray)() | Görüntünün depolanmış veya bağlantılı olmasına bakılmaksızın herhangi bir görüntü için görüntü baytlarını döndürür. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage)() | Şekilde depolanan görüntüyü birImage nesne. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream)() | Görüntü baytlarını içeren bir akış oluşturur ve döndürür. |

### Notlar

Kullan[`ImageData`](../shape/imagedata) bir şeklin içindeki resme erişme ve onu değiştirme özelliği. [`ImageData`](../imagedata) doğrudan sınıf.

Bir görüntü, bir şeklin içinde, harici dosyaya bağlı olarak veya her ikisinde de saklanabilir (bağlantılı ve belgede saklanabilir).

Resmin şeklin içinde mi yoksa bağlantılı olarak mı saklandığına bakılmaksızın, her zaman aktüel resmine şu komutu kullanarak erişebilirsiniz:[`ToByteArray`](./tobytearray) ,[`ToStream`](./tostream) ,[`ToImage`](./toimage) veya[`Save`](./save) yöntemleri. Görüntü şeklin içinde saklanıyorsa, aynı zamanda[`ImageBytes`](./imagebytes) Emlak.

Bir resmi bir şeklin içinde saklamak için[`SetImage`](./setimage) yöntem. Bir görüntüyü bir şekle bağlamak için[`SourceFullName`](./sourcefullname) Emlak.

### Örnekler

Bir belgeden görüntülerin nasıl çıkarılacağını ve bunların yerel dosya sistemine ayrı dosyalar olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgeden şekil koleksiyonunu alın,
// ve bir görüntü ile her şeklin görüntü verilerini yerel dosya sistemine dosya olarak kaydedin.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Şekillerin görüntü verileri, birçok olası görüntü formatının görüntülerini içerebilir. 
        // Her resim için formatına göre otomatik olarak bir dosya uzantısı belirleyebiliriz.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Bir belgeye bağlantılı bir görüntünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Aşağıda, bir şekli gösterebilmesi için bir şekle bir resim uygulamanın iki yolu verilmiştir.
// 1 - Resmi içerecek şekli ayarlayın.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Formda sakladığımız her resim belgemizin boyutunu artıracaktır.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Yerel dosya sistemindeki bir görüntü dosyasına bağlanacak şekli ayarlayın.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Resimlere bağlantı vermek yerden tasarruf sağlar ve daha küçük bir belgeyle sonuçlanır.
// Ancak, belge yalnızca görüntüyü doğru olarak görüntüleyebilir.
// görüntü dosyası, şeklin "SourceFullName" özelliğinin işaret ettiği konumda bulunur.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
