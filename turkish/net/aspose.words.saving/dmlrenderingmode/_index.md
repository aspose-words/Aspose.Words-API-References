---
title: DmlRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: DrawingML şekillerinin nasıl sabit sayfa biçimlerine dönüştürüleceğini belirtir.
type: docs
weight: 4660
url: /tr/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

DrawingML şekillerinin nasıl sabit sayfa biçimlerine dönüştürüleceğini belirtir.

```csharp
public enum DmlRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Fallback | `0` | DrawingML için geri dönüş şekli mevcutsa, Aspose.Words DrawingML yerine geri dönüş şekli işler. |
| DrawingML | `1` | Aspose.Words, DrawingML'nin geri dönüş şeklini yok sayar ve DrawingML'nin kendisini oluşturur. Bu, varsayılan moddur. |

### Örnekler

PDF'ye kaydederken yedek şekillerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// "DmlRenderingMode" özelliğini "DmlRenderingMode.Fallback" olarak ayarlayın
// DML şekillerini yedek şekilleriyle değiştirmek için.
// "DmlRenderingMode" özelliğini "DmlRenderingMode.DrawingML" olarak ayarlayın
// DML şekillerini kendileri oluşturmak için.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Bir belgeyi PDF'ye kaydederken, DrawingML efektlerinin oluşturma kalitesinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Tüm DrawingML efektlerini atmak için "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.None" olarak ayarlayın.
// "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.Simplified" olarak ayarlayın
// DrawingML efektlerinin basitleştirilmiş bir sürümünü oluşturmak için.
// "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.Fine" olarak ayarlayın.
// DrawingML efektlerini daha doğru bir şekilde ve ayrıca daha fazla işlem maliyetiyle işleyin.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
