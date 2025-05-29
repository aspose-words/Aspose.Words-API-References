---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: .NET için Aspose.Words
description: Sabit sayfa formatlarında optimize edilmiş DrawingML efekt işleme için Aspose.Words DmlEffectsRenderingMode enum'unu keşfedin. Belge kalitenizi artırın!
type: docs
weight: 5660
url: /tr/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

DrawingML efektlerinin sabit sayfa biçimlerine nasıl işleneceğini belirtir.

```csharp
public enum DmlEffectsRenderingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Simplified | `0` | DrawingML efektlerinin işlenmesi basitleştirildi. |
| None | `1` | Hiçbir DrawingML efekti oluşturulmadı. |
| Fine | `2` | DrawingML efektleri, gelişmiş işlemeyi içeren ince modda işlenir. Bu modda efektlerin işlenmesi daha iyi sonuçlar verir ancak daha yüksek bir performans maliyetiyle.Simplified mod. |

## Örnekler

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
