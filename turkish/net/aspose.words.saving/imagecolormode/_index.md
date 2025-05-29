---
title: ImageColorMode Enum
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: .NET için Aspose.Words
description: Belge sayfa görüntülerini optimize etmek için Aspose.Words.Saving.ImageColorMode enum'unu keşfedin. Projelerinizde gelişmiş görsel kalite için renk modlarını kontrol edin.
type: docs
weight: 5960
url: /tr/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

Belge sayfalarının oluşturulan görüntüleri için renk modunu belirtir.

```csharp
public enum ImageColorMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Belgenin sayfaları renkli resimler olarak işlenecektir. |
| Grayscale | `1` | Belgenin sayfaları gri tonlamalı görüntüler olarak işlenecektir. |
| BlackAndWhite | `2` | Belgenin sayfaları siyah beyaz resimler olarak gösterilecektir. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
