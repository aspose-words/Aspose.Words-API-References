---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: .NET için Aspose.Words
description: Oluşturduğunuz görsellerin piksel biçimini en iyi kalite ve performans için kolayca özelleştirmek amacıyla ImageSaveOptions PixelFormat özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Oluşturulan görüntülerin piksel biçimini alır veya ayarlar.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Notlar

Bu özellik yalnızca raster görüntü formatlarına kaydedilirken etkilidir.

Varsayılan değer:Format32BppArgb.

GDI+'ın çalışmasından dolayı çıkış görüntüsünün piksel biçimi ayarlanan değerden farklı olabilir.

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

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
