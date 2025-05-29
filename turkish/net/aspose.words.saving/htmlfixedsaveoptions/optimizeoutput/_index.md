---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: .NET için Aspose.Words
description: HTML çıktınızı HtmlFixedSaveOptions özelliğiyle optimize edin. Gereksiz tuvalleri kaldırarak ve benzer glifleri birleştirerek performansı artırın. Varsayılan, true.
type: docs
weight: 110
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Bayrağı, çıktının optimize edilmesinin gerekip gerekmediğini belirtir. Bu bayrak ayarlanırsa, gereksiz iç içe geçmiş tuvaller ve boş tuvaller kaldırılır, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Bu özellik olarak ayarlanırsa içerik görüntüsünün doğruluğu etkilenebilir.`doğru` . Varsayılan`doğru` .

```csharp
public override bool OptimizeOutput { get; set; }
```

## Örnekler

Çeşitli gereksiz nesneleri kaldırarak bir belgeyi HTML'e kaydederken belgenin nasıl basitleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// Belgenin optimize edilmiş sürümünün boyutu, optimize edilmemiş belgenin boyutunun neredeyse üçte biri kadardır.
Assert.AreEqual(optimizeOutput ? 60385 : 191000,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
