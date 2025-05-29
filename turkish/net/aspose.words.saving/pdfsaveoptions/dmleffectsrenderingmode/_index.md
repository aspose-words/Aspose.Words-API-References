---
title: PdfSaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: .NET için Aspose.Words
description: Gelişmiş PDF çıktı kalitesi için DrawingML efektlerinin işlenmesini kontrol etmek üzere PdfSaveOptions DmlEffectsRenderingMode özelliğini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Notlar

Varsayılan değer:Simplified .

Bu özellik, belge sabit sayfa biçimlerine aktarıldığında kullanılır.

Eğer[`Compliance`](../compliance/) ayarlandıPdfA1a veyaPdfA1b , özelliği her zaman dönerNone.

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
