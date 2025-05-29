---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: .NET için Aspose.Words
description: SaveOptions DmlRenderingMode özelliğinin DrawingML şekil oluşturmanızı nasıl geliştirdiğini keşfedin. Belge görsellerinizi zahmetsizce optimize edin!
type: docs
weight: 70
url: /tr/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

DrawingML şekillerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## Notlar

Varsayılan değer:Fallback .

Bu özellik, belge sabit sayfa biçimlerine aktarıldığında kullanılır.

## Örnekler

PDF'e kaydederken yedek şekillerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// "DmlRenderingMode" özelliğini "DmlRenderingMode.Fallback" olarak ayarlayın
// DML şekillerini yedek şekilleriyle değiştirmek için.
// "DmlRenderingMode" özelliğini "DmlRenderingMode.DrawingML" olarak ayarlayın
// DML şekillerinin kendilerini oluşturmak için.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Bir belgeyi PDF olarak kaydederken DrawingML efektlerinin işleme kalitesinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Tüm DrawingML efektlerini atmak için "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.None" olarak ayarlayın.
// "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.Simplified" olarak ayarlayın
// DrawingML efektlerinin basitleştirilmiş bir versiyonunu oluşturmak için.
// "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.Fine" olarak ayarlayın
// DrawingML efektlerini daha yüksek doğrulukla ve daha yüksek işlem maliyetiyle işleyin.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Ayrıca bakınız

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
