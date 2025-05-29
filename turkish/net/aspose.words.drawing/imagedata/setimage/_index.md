---
title: ImageData.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: .NET için Aspose.Words
description: Şekillerinizi özelleştirilmiş görsellerle geliştirmek için ImageData'daki SetImage metodunu nasıl kullanacağınızı keşfedin. Tasarımınızı zahmetsizce yükseltin!
type: docs
weight: 210
url: /tr/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(*Image*) {#setimage}

Şeklin görüntülediği görüntüyü ayarlar.

```csharp
public void SetImage(Image image)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Resim nesnesi. |

## Örnekler

Yerel dosya sistemindeki resimlerin bir belgede nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();

// Bir belgede bir görüntüyü görüntülemek için bir şekil oluşturmamız gerekecek
// içerisinde bir resim bulunacak ve daha sonra bu resim belgenin gövdesine eklenecektir.
Shape imgShape;

// Aşağıda yerel dosya sistemindeki bir dosyadan görüntü almanın iki yolu bulunmaktadır.
// 1 - Bir resim dosyasından bir resim nesnesi oluştur:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Bir akış kullanarak yerel dosya sisteminden bir görüntü dosyası açın:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Ayrıca bakınız

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Şeklin görüntülediği görüntüyü ayarlar.

```csharp
public void SetImage(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Görüntüyü içeren akış. |

## Örnekler

Yerel dosya sistemindeki resimlerin bir belgede nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();

// Bir belgede bir görüntüyü görüntülemek için bir şekil oluşturmamız gerekecek
// içerisinde bir resim bulunacak ve daha sonra bu resim belgenin gövdesine eklenecektir.
Shape imgShape;

// Aşağıda yerel dosya sistemindeki bir dosyadan görüntü almanın iki yolu bulunmaktadır.
// 1 - Bir resim dosyasından bir resim nesnesi oluştur:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Bir akış kullanarak yerel dosya sisteminden bir görüntü dosyası açın:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Ayrıca bakınız

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(*string*) {#setimage_2}

Şeklin görüntülediği görüntüyü ayarlar.

```csharp
public void SetImage(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resim dosyası. Bir dosya adı veya URL olabilir. |

## Örnekler

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

* class [ImageData](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
