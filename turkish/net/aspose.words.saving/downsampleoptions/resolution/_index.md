---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: .NET için Aspose.Words
description: Üstün alt örnekleme sonuçları için inç başına ideal piksel sayısını tanımlayarak, DownsampleOptions Çözünürlük özelliğiyle görüntü kalitesini iyileştirin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Görüntülerin aşağı örneklenmesi gereken inç başına piksel cinsinden çözünürlüğü belirtir.

```csharp
public int Resolution { get; set; }
```

## Notlar

Varsayılan değer 220 ppi'dir.

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
