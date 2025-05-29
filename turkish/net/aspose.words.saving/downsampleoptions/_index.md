---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: .NET için Aspose.Words
description: Optimize edilmiş belge kalitesi ve performansı için görüntü alt örneklemesini kolayca özelleştirmek amacıyla Aspose.Words.Saving.DownsampleOptions sınıfını keşfedin.
type: docs
weight: 5720
url: /tr/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Alt örnekleme seçeneklerini belirtmeye izin verir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

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
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Görüntülerin örnekleminin küçültülüp küçültülmeyeceğini belirtir. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Görüntülerin aşağı örneklenmesi gereken inç başına piksel cinsinden çözünürlüğü belirtir. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | İnç başına piksel cinsinden eşik çözünürlüğünü belirtir. Belgedeki bir görüntünün çözünürlüğü eşik değerinden düşükse, alt örnekleme algoritması uygulanmaz. 0 değeri, eşik denetiminin kullanılmadığı ve boyutu azaltılabilen tüm görüntülerin alt örneklemesinin yapıldığı anlamına gelir. |

## Örnekler

PDF belgesindeki resimlerin çözünürlüğünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Varsayılan olarak, Aspose.Words PDF'ye kaydettiğimiz bir belgedeki tüm görselleri 220 ppi'ye düşürür.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Tüm görüntüleri 36 ppi'ye düşürmek için "Çözünürlük" özelliğini "36" olarak ayarlayın.
options.DownsampleOptions.Resolution = 36;

// "ResolutionThreshold" özelliğini yalnızca alt örneklemeyi uygulayacak şekilde ayarlayın
// Çözünürlüğü 128 ppi'nin üzerinde olan görüntüler.
options.DownsampleOptions.ResolutionThreshold = 128;

// Bu aşamada yalnızca belgedeki ilk iki görüntü küçültülecek.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
