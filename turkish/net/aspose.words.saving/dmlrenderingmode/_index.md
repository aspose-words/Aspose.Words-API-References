---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.DmlRenderingMode Sıralama. DrawingML şekillerinin sabit sayfa formatlarına nasıl aktarılacağını belirtir C#'da.
type: docs
weight: 4920
url: /tr/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

DrawingML şekillerinin sabit sayfa formatlarına nasıl aktarılacağını belirtir.

```csharp
public enum DmlRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Fallback | `0` | Eğer DrawingML için geri dönüş şekli mevcutsa Aspose.Words, DrawingML yerine geri dönüş şekli oluşturur. |
| DrawingML | `1` | Aspose.Words, DrawingML'in geri dönüş şeklini yok sayar ve DrawingML'in kendisini oluşturur. Bu, varsayılan moddur. |

## Örnekler

PDF'ye kaydederken geri dönüş şekillerinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// "DmlRenderingMode" özelliğini "DmlRenderingMode.Fallback" olarak ayarlayın
// DML şekillerini geri dönüş şekilleriyle değiştirmek için.
// "DmlRenderingMode" özelliğini "DmlRenderingMode.DrawingML" olarak ayarlayın
// DML şekillerini kendileri oluşturmak için.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Bir belgeyi PDF'ye kaydederken, DrawingML efektlerinin görüntü oluşturma kalitesinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Tüm DrawingML efektlerini atmak için "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.None" olarak ayarlayın.
// "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.Simplified" olarak ayarlayın
// DrawingML efektlerinin basitleştirilmiş bir versiyonunu oluşturmak için.
// "DmlEffectsRenderingMode" özelliğini "DmlEffectsRenderingMode.Fine" olarak ayarlayın
// DrawingML efektlerini daha doğru ve aynı zamanda daha fazla işlem maliyetiyle işleyin.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
