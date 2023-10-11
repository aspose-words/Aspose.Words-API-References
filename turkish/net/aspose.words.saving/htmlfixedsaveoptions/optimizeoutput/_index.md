---
title: HtmlFixedSaveOptions.OptimizeOutput
second_title: Aspose.Words for .NET API Referansı
description: HtmlFixedSaveOptions mülk. Bayrak çıktıyı optimize etmenin gerekli olup olmadığını belirtir. Bu bayrak ayarlanırsa yedekli iç içe tuvaller ve boş tuvaller kaldırılır aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir bu özellik şu şekilde ayarlandıdoğru . Varsayılandoğru .
type: docs
weight: 100
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Bayrak, çıktıyı optimize etmenin gerekli olup olmadığını belirtir. Bu bayrak ayarlanırsa, yedekli iç içe tuvaller ve boş tuvaller kaldırılır, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Aşağıdaki durumlarda içerik görüntüsünün doğruluğu etkilenebilir: bu özellik şu şekilde ayarlandı:`doğru` . Varsayılan:`doğru` .

```csharp
public override bool OptimizeOutput { get; set; }
```

### Örnekler

Çeşitli gereksiz nesneleri kaldırarak bir belgeyi HTML'ye kaydederken nasıl basitleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// Belgenin optimize edilmiş sürümünün boyutu, optimize edilmemiş belgenin neredeyse üçte biri kadardır.
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* toplantı [Aspose.Words](../../../)


