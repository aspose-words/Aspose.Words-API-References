---
title: PdfSaveOptions.DownsampleOptions
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Altörnekleme seçeneklerini belirlemeye izin verir.
type: docs
weight: 100
url: /tr/net/aspose.words.saving/pdfsaveoptions/downsampleoptions/
---
## PdfSaveOptions.DownsampleOptions property

Altörnekleme seçeneklerini belirlemeye izin verir.

```csharp
public DownsampleOptions DownsampleOptions { get; set; }
```

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

* class [DownsampleOptions](../../downsampleoptions/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


