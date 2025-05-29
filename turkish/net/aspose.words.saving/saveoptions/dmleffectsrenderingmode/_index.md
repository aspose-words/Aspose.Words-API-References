---
title: SaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: .NET için Aspose.Words
description: SaveOptions DmlEffectsRenderingMode özelliğinin, gelişmiş belge kalitesi ve performansı için DrawingML efektlerinin işlenmesini nasıl optimize ettiğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

DrawingML efektlerinin nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Notlar

Varsayılan değer:Simplified .

Bu özellik, belge sabit sayfa biçimlerine aktarıldığında kullanılır.

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
* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
