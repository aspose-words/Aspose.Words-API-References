---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: .NET için Aspose.Words
description: SaveOptions MemoryOptimization özelliğiyle belge performansını artırın. Kaydetmeden önce bellek kullanımını kontrol edin, verimliliği ve hızı artırın.
type: docs
weight: 100
url: /tr/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Belgeyi kaydetmeden önce bellek optimizasyonunun yapılıp yapılmayacağını belirleyen değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`YANLIŞ` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Notlar

Bu seçeneği ayarlamak`doğru` Büyük belgeleri kaydederken bellek tüketimini önemli ölçüde azaltabilir ancak daha yavaş kaydetme süresi pahasına.

## Örnekler

Büyük belgeleri PDF'ye dönüştürürken bellek tüketimini optimize etmek için bir seçenek gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Büyük belgelerin kaydetme işlemlerinin bellek ayak izini azaltmak için "MemoryOptimization" özelliğini "true" olarak ayarlayın
// operasyonun süresinin artması pahasına.
// Belgeyi normal şekilde PDF olarak kaydetmek için "MemoryOptimization" özelliğini "false" olarak ayarlayın.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
