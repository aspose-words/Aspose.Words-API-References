---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: .NET için Aspose.Words
description: Oluşturduğunuz görseller için renk modunu kolayca özelleştirmek ve optimize etmek için ImageSaveOptions ImageColorMode özelliğini keşfedin. Görsellerinizi bugün geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Oluşturulan görüntüler için renk modunu alır veya ayarlar.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## Notlar

Bu özellik yalnızca raster görüntü formatlarına kaydedilirken etkilidir.

Varsayılan değer:None.

## Örnekler

Belgeleri işlerken renk modunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi bir resim olarak kaydettiğimizde, SaveOptions nesnesini görüntüye geçirebiliriz.
// Kaydetme işleminin üreteceği görüntü için bir renk modu seçin.
// "ImageColorMode" özelliğini "ImageColorMode.BlackAndWhite" olarak ayarlarsak,
// Kaydetme işlemi, belgenin işlenmesi sırasında gri tonlamalı renk azaltımını uygulayacaktır.
 // "ImageColorMode" özelliğini "ImageColorMode.Grayscale" olarak ayarlarsak,
// kaydetme işlemi belgeyi monokrom bir görüntüye dönüştürecektir.
// "ImageColorMode" özelliğini "Hiçbiri" olarak ayarlarsak, kaydetme işlemi varsayılan yöntemi uygulayacaktır
// ve çıktı görüntüsünde belgenin tüm renklerini koru.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Ayrıca bakınız

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
