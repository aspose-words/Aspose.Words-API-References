---
title: Class DownsampleOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.DownsampleOptions sınıf. Altörnekleme seçeneklerini belirlemeye izin verir.
type: docs
weight: 4970
url: /tr/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Altörnekleme seçeneklerini belirlemeye izin verir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) dokümantasyon makalesi.

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
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Görüntülerin altörneklenmesi gereken çözünürlüğü inç başına piksel cinsinden belirtir. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Eşik çözünürlüğünü inç başına piksel cinsinden belirtir. Belgedeki bir görüntünün çözünürlüğü eşik değerinden düşükse, alt örnekleme algoritması uygulanmaz. 0 değeri, eşik kontrolünün kullanılmadığı ve eşik değerinin kullanılmadığı anlamına gelir boyutu küçültülebilir, altörneklenir. |

### Örnekler

PDF belgesindeki görüntülerin çözünürlüğünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Varsayılan olarak Aspose.Words, PDF'ye kaydettiğimiz bir belgedeki tüm görselleri 220 ppi'ye altörnekler.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Tüm görüntüleri 36 ppi'ye alt örneklemek için "Çözünürlük" özelliğini "36" olarak ayarlayın.
options.DownsampleOptions.Resolution = 36;

// "ResolutionThreshold" özelliğini yalnızca alt örneklemeyi uygulayacak şekilde ayarlayın
// çözünürlüğü 128 ppi'nin üzerinde olan resimler.
options.DownsampleOptions.ResolutionThreshold = 128;

// Bu aşamada belgedeki yalnızca ilk iki görüntünün alt örneği alınacaktır.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


