---
title: ImageSaveOptions.PaperColor
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. Oluşturulan görüntüler için arka plan kağıt rengini alır veya ayarlar.
type: docs
weight: 100
url: /tr/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Oluşturulan görüntüler için arka plan (kağıt) rengini alır veya ayarlar.

Varsayılan değerWhite.

```csharp
public Color PaperColor { get; set; }
```

### Notlar

Kendi arka plan rengini, belirten bir belgenin sayfalarını oluştururken, belge arka plan rengi bu özellik tarafından belirtilen rengi geçersiz kılar.

### Örnekler

Bir Word belgesinin bir sayfasını saydam veya renkli arka plana sahip bir görüntüye dönüştürür.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Saydam bir renk uygulamak için "PaperColor" özelliğini saydam bir renge ayarlayın
// bir görüntüye dönüştürülürken belgenin arka planı.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// "PaperColor" özelliğini o rengi uygulamak için opak bir renge ayarlayın
// bir görüntüye dönüştürürken belgenin arka planı olarak.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


