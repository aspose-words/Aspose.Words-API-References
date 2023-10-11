---
title: ImageSaveOptions.PaperColor
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. Oluşturulan görüntüler için arka plan kağıt rengini alır veya ayarlar.
type: docs
weight: 110
url: /tr/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Oluşturulan görüntüler için arka plan (kağıt) rengini alır veya ayarlar.

Varsayılan değer:White.

```csharp
public Color PaperColor { get; set; }
```

### Notlar

Kendi arka plan rengini ( ) belirten bir belgenin sayfaları oluşturulurken, belgenin arka plan rengi bu özellik tarafından belirtilen rengi geçersiz kılacaktır.

### Örnekler

Word belgesinin bir sayfasını şeffaf veya renkli arka plana sahip bir görüntüye dönüştürür.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Şeffaf renk uygulamak için "PaperColor" özelliğini şeffaf renge ayarlayın
// belgeyi bir görüntüye dönüştürürken arka planı.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Bu rengi uygulamak için "PaperColor" özelliğini opak bir renge ayarlayın
// belgeyi bir görüntüye dönüştürdüğümüzde arka plan olarak.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


