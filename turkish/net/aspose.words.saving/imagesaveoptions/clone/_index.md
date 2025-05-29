---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: Nesnelerinizin derin bir klonunu zahmetsizce oluşturmak, kodlama verimliliğinizi ve esnekliğinizi artırmak için ImageSaveOptions Clone yöntemini keşfedin.
type: docs
weight: 210
url: /tr/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

Bu nesnenin derin bir klonunu oluşturur.

```csharp
public ImageSaveOptions Clone()
```

## Örnekler

Bir belgenin görüntüye dönüştürülmesi için bit/piksel oranının nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi bir resim olarak kaydettiğimizde, SaveOptions nesnesini görüntüye geçirebiliriz.
// kaydetme işleminin üreteceği görüntü için bir piksel formatı seçin.
// Çeşitli bit/piksel oranları, oluşturulan görüntünün kalitesini ve dosya boyutunu etkileyecektir.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// ImageSaveOptions örneklerini klonlayabiliriz.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
