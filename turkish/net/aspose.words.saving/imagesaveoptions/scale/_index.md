---
title: ImageSaveOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: .NET için Aspose.Words
description: Görüntülerinizin yakınlaştırma faktörünü zahmetsizce ayarlamak, kaliteyi ve özelleştirmeyi geliştirmek için ImageSaveOptions Ölçek özelliğini keşfedin.
type: docs
weight: 150
url: /tr/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Oluşturulan görüntüler için yakınlaştırma faktörünü alır veya ayarlar.

```csharp
public float Scale { get; set; }
```

## Notlar

Varsayılan değer 1.0'dır. Değer 0'dan büyük olmalıdır.

## Örnekler

Office Math nesnesinin yerel dosya sisteminde bir görüntü dosyasına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Düğüm oluşturucusunun "Kaydet" yöntemine geçirilecek ve değiştirilecek bir "ImageSaveOptions" nesnesi oluşturun
// OfficeMath düğümünü bir görüntüye nasıl dönüştürdüğü.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Nesneyi orijinal boyutunun beş katına çıkarmak için "Ölçek" özelliğini 5 olarak ayarlayın.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

Aspose.Words'ün bir belgeyi bir belgeye dönüştürmesini sağlarken görüntünün nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi bir resim olarak kaydettiğimizde, SaveOptions nesnesini görüntüye geçirebiliriz.
// Kaydetme işlemi sırasında görüntüyü düzenle.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Görüntünün parlaklığını ve kontrastını değiştirmek için bu özellikleri ayarlayabiliriz.
    // Her ikisi de 0-1 ölçeğindedir ve varsayılan olarak 0,5'tir.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Bu özellikler ile yatay ve dikey çözünürlüğü ayarlayabiliriz.
    // Bu, görüntünün boyutlarını etkileyecektir.
    // Bu özelliklerin varsayılan değeri 96 dpi çözünürlük için 96.0'dır.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Bu özelliği kullanarak görüntüyü ölçekleyebiliriz. Varsayılan değer %100 ölçekleme için 1.0'dır.
    // Bu özelliği, çözünürlüğü değiştirmenin görüntü boyutlarında neden olacağı değişiklikleri ortadan kaldırmak için kullanabiliriz.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
