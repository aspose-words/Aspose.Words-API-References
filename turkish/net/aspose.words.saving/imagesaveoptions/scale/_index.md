---
title: ImageSaveOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words for .NET
description: ImageSaveOptions Scale mülk. Oluşturulan görüntüler için yakınlaştırma faktörünü alır veya ayarlar C#'da.
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

Varsayılan değer 1,0'dır. Değer 0. 'den büyük olmalıdır

## Örnekler

Bir Office Math nesnesinin yerel dosya sistemindeki bir görüntü dosyasına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Değiştirmek üzere düğüm oluşturucunun "Kaydet" yöntemine iletilecek bir "ImageSaveOptions" nesnesi oluşturun
// OfficeMath düğümünü bir görüntüye nasıl dönüştürdüğü.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Nesneyi orijinal boyutunun beş katına çıkarmak için "Ölçek" özelliğini 5'e ayarlayın.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

Aspose.Words bir belgeyi belgeye dönüştürürken görüntünün nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi resim olarak kaydettiğimizde, bir SaveOptions nesnesini iletebiliriz
// kaydetme işlemi onu oluştururken görüntüyü düzenleyin.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Görüntünün parlaklığını ve kontrastını değiştirmek için bu özellikleri ayarlayabiliriz.
    // Her ikisi de 0-1 ölçeğindedir ve varsayılan olarak 0,5'tir.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Bu özelliklerle yatay ve dikey çözünürlüğü ayarlayabiliriz.
    // Bu görüntünün boyutlarını etkileyecektir.
    // Bu özelliklerin varsayılan değeri 96 dpi çözünürlük için 96,0'dır.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Bu özelliği kullanarak görüntüyü ölçeklendirebiliriz. %100 ölçeklendirme için varsayılan değer 1,0'dır.
    // Bu özelliği, çözünürlük değişikliğinin görüntü boyutlarında neden olacağı değişiklikleri engellemek için kullanabiliriz.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
