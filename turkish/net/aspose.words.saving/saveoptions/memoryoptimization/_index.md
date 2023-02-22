---
title: SaveOptions.MemoryOptimization
second_title: Aspose.Words for .NET API Referansı
description: SaveOptions mülk. Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer yanlış .
type: docs
weight: 110
url: /tr/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özellik için varsayılan değer **yanlış** .

```csharp
public bool MemoryOptimization { get; set; }
```

### Notlar

Bu seçeneği true olarak ayarlamak bellek tüketimini önemli ölçüde azaltırken, büyük belgeleri daha yavaş tasarruf süresi pahasına kaydeder.

### Örnekler

Büyük belgeleri PDF'ye dönüştürürken bellek tüketimini optimize etme seçeneği gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Büyük belgelerin kaydetme işlemlerinin bellek kapladığı alanı azaltmak için "MemoryOptimization" özelliğini "true" olarak ayarlayın
// operasyon süresini artırma pahasına.
// Belgeyi normal olarak PDF olarak kaydetmek için "MemoryOptimization" özelliğini "false" olarak ayarlayın.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../saveoptions/)
* toplantı [Aspose.Words](../../../)


