---
title: Class DownsampleOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.DownsampleOptions sınıf. Alt örnek seçeneklerini belirlemeye izin verir.
type: docs
weight: 4710
url: /tr/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Alt örnek seçeneklerini belirlemeye izin verir.

```csharp
public class DownsampleOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [DownsampleOptions](downsampleoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Görüntülerin altörneklenmesi gerekip gerekmediğini belirtir. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Görüntülerin altörneklenmesi gereken inç başına piksel cinsinden çözünürlüğü belirtir. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | İnç başına piksel cinsinden eşik çözünürlüğünü belirtir. Belgedeki bir görüntünün çözünürlüğü eşik değerinden düşükse, altörnekleme algoritması uygulanmaz. 0 değeri, eşik denetiminin kullanılmadığı ve tüm görüntülerin boyut olarak küçültülebilir, altörneklenir. |

### Örnekler

PDF belgesindeki görüntülerin çözünürlüğünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Varsayılan olarak Aspose.Words, PDF'ye kaydettiğimiz bir belgedeki tüm görüntüleri 220 ppi'ye düşürür.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Tüm görüntüleri 36 ppi'ye düşürmek için "Çözünürlük" özelliğini "36" olarak ayarlayın.
options.DownsampleOptions.Resolution = 36;

// "ResolutionThreshold" özelliğini yalnızca altörneklemeyi
// çözünürlüğü 128 ppi'nin üzerinde olan görüntüler.
options.DownsampleOptions.ResolutionThreshold = 128;

// Bu aşamada belgeden yalnızca ilk iki görüntü altörneklenecektir.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


