---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words for .NET
description: SaveOptions MemoryOptimization mülk. Belgeyi kaydetmeden önce bellek optimizasyonunun gerçekleştirilip gerçekleştirilmeyeceğini belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Belgeyi kaydetmeden önce bellek optimizasyonunun gerçekleştirilip gerçekleştirilmeyeceğini belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer:`YANLIŞ` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Notlar

Bu seçeneği şu şekilde ayarlıyoruz:`doğru` büyük belgeleri kaydederken, daha yavaş kaydetme süresi pahasına bellek tüketimini önemli ölçüde azaltabilir.

## Örnekler

Büyük belgeleri PDF'ye dönüştürürken bellek tüketimini optimize etme seçeneğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Büyük belgelerin kaydetme işlemlerinin bellek alanını azaltmak için "MemoryOptimization" özelliğini "true" olarak ayarlayın
// operasyonun süresini arttırma pahasına.
// Belgeyi normal şekilde PDF olarak kaydetmek için "MemoryOptimization" özelliğini "false" olarak ayarlayın.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
