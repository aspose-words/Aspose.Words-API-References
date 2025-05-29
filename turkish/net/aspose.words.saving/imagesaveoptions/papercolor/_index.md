---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: .NET için Aspose.Words
description: Oluşturduğunuz görsellerin arka plan renklerini kolayca özelleştirmek, görsel çekiciliği ve benzersizliği artırmak için ImageSaveOptions PaperColor özelliğini keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Oluşturulan resimler için arka plan (kağıt) rengini alır veya ayarlar.

Varsayılan değer:White.

```csharp
public Color PaperColor { get; set; }
```

## Notlar

Kendi arka plan rengini belirten bir belgenin sayfaları işlenirken, , belgenin arka plan rengi bu özellik tarafından belirtilen rengi geçersiz kılacaktır.

## Örnekler

Word belgesinin bir sayfasını şeffaf veya renkli arka planlı bir görüntüye dönüştürür.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// Şeffaf bir renk uygulamak için "PaperColor" özelliğini şeffaf bir renge ayarlayın
// belgenin görüntüye dönüştürülmesi sırasında arka plan olarak kullanılır.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Bu rengi uygulamak için "PaperColor" özelliğini opak bir renge ayarlayın
// belgeyi bir görüntüye dönüştürdüğümüzde arka plan olarak kullanırız.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
