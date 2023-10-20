---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words for .NET
description: FixedPageSaveOptions OptimizeOutput mülk. Bayrak çıktıyı optimize etmenin gerekli olup olmadığını belirtir. Bu bayrak ayarlanırsa yedekli iç içe tuvaller ve boş tuvaller kaldırılır ayrıca aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir bu özellik şu şekilde ayarlandıdoğru . VarsayılanYANLIŞ  C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Bayrak, çıktıyı optimize etmenin gerekli olup olmadığını belirtir. Bu bayrak ayarlanırsa, yedekli iç içe tuvaller ve boş tuvaller kaldırılır, ayrıca aynı biçimlendirmeye sahip komşu glifler birleştirilir. Not: Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir: bu özellik şu şekilde ayarlandı:`doğru` . Varsayılan:`YANLIŞ` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Örnekler

Xps'e kaydederken belge nesnelerinin nasıl optimize edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Belgenin "Kaydet" yöntemine geçmek için bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e dönüştürme biçimini değiştirmek için.
XpsSaveOptions saveOptions = new XpsSaveOptions();

// İç içe geçmiş veya boş tuvalleri kaldırmak gibi önlemleri almak için "OptimizeOutput" özelliğini "true" olarak ayarlayın
// ve çıktı belgesinin içeriğini optimize etmek için bitişik işlemleri aynı biçimlendirmeyle birleştiriyor.
// Bu, belgenin görünümünü etkileyebilir.
// Belgeyi normal şekilde kaydetmek için "OptimizeOutput" özelliğini "false" olarak ayarlayın.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
