---
title: DownsampleOptions.ResolutionThreshold
linktitle: ResolutionThreshold
articleTitle: ResolutionThreshold
second_title: .NET için Aspose.Words
description: Görüntülerinizi DownsampleOptions ResolutionThreshold özelliğiyle optimize edin. Daha iyi performans ve kalite için çözünürlüğe dayalı alt örneklemeyi kontrol edin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

İnç başına piksel cinsinden eşik çözünürlüğünü belirtir. Belgedeki bir görüntünün çözünürlüğü eşik değerinden düşükse, alt örnekleme algoritması uygulanmaz. 0 değeri, eşik denetiminin kullanılmadığı ve boyutu azaltılabilen tüm görüntülerin alt örneklemesinin yapıldığı anlamına gelir.

```csharp
public int ResolutionThreshold { get; set; }
```

## Notlar

Varsayılan değer 0'dır.

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

* class [DownsampleOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
