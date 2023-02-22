---
title: FixedPageSaveOptions.OptimizeOutput
second_title: Aspose.Words for .NET API Referansı
description: FixedPageSaveOptions mülk. Bayrak çıktının optimize edilmesinin gerekip gerekmediğini gösterir. Bu bayrak ayarlanırsa fazladan iç içe tuvaller ve boş tuvaller kaldırılırsa aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir bu özellik true olarak ayarlanmıştır. Varsayılan değer falsetur.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Bayrak, çıktının optimize edilmesinin gerekip gerekmediğini gösterir. Bu bayrak ayarlanırsa, fazladan iç içe tuvaller ve boş tuvaller kaldırılırsa, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir: bu özellik true olarak ayarlanmıştır. Varsayılan değer false'tur.

```csharp
public virtual bool OptimizeOutput { get; set; }
```

### Örnekler

xps'e kaydederken belge nesnelerinin nasıl optimize edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Belgenin "Kaydet" yöntemine geçmek için bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'ye dönüştürme şeklini değiştirmek için.
XpsSaveOptions saveOptions = new XpsSaveOptions();

// İç içe geçmiş veya boş tuvalleri kaldırmak gibi önlemler almak için "OptimizeOutput" özelliğini "true" olarak ayarlayın
// ve çıktı belgesinin içeriğini optimize etmek için aynı biçimlendirmeyle bitişik çalıştırmaları birleştirmek.
// Bu, belgenin görünümünü etkileyebilir.
// Belgeyi normal şekilde kaydetmek için "OptimizeOutput" özelliğini "false" olarak ayarlayın.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* toplantı [Aspose.Words](../../../)


