---
title: Enum DmlEffectsRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.DmlEffectsRenderingMode Sıralama. DrawingML efektlerinin sabit sayfa formatlarına nasıl aktarılacağını belirtir.
type: docs
weight: 4910
url: /tr/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

DrawingML efektlerinin sabit sayfa formatlarına nasıl aktarılacağını belirtir.

```csharp
public enum DmlEffectsRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Simplified | `0` | DrawingML efektlerinin oluşturulması basitleştirildi. |
| None | `1` | Hiçbir DrawingML efekti oluşturulmaz. |
| Fine | `2` | DrawingML efektleri, gelişmiş işlemeyi içeren hassas modda oluşturulur. Bu modda efektlerin oluşturulması, daha iyi sonuçlar verir ancak daha yüksek bir performans maliyetiyle sağlanır.Simplified mode. |

### Örnekler

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


