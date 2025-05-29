---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.DmlRenderingMode'un yüksek kaliteli sabit sayfa biçimleri için DrawingML şekil oluşturmayı nasıl geliştirdiğini keşfedin. Belge görsellerinizi optimize edin!
type: docs
weight: 5670
url: /tr/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

DrawingML şekillerinin sabit sayfa biçimlerine nasıl işleneceğini belirtir.

```csharp
public enum DmlRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Fallback | `0` | DrawingML için geri çekilme şekli mevcutsa, Aspose.Words, DrawingML yerine geri çekilme şeklini işler. |
| DrawingML | `1` | Aspose.Words, DrawingML'in geri çekilme şeklini yok sayar ve DrawingML'in kendisini işler. Bu varsayılan moddur. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
