---
title: PdfSaveOptions.DmlEffectsRenderingMode
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

DrawingML efektlerinin nasıl oluşturulacağını belirleyen bir değer alır veya ayarlar.

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

### Notlar

Varsayılan değer:Simplified .

Bu özellik, belge sabit sayfa formatlarına aktarıldığında kullanılır.

Eğer[`Compliance`](../compliance/) ayarlandıPdfA1a veyaPdfA1b , özelliği her zaman döndürürNone.

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


