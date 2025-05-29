---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: .NET için Aspose.Words
description: FixedPageSaveOptions' OptimizeOutput özelliğiyle belge çıktınızı geliştirin. Fazlalıkları kaldırın ve daha net görüntüler için biçimlendirmeyi iyileştirin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Bayrağı, çıktının optimize edilmesinin gerekip gerekmediğini belirtir. Bu bayrak ayarlanırsa, gereksiz iç içe geçmiş tuvaller ve boş tuvaller kaldırılır, aynı biçimlendirmeye sahip komşu glifler de birleştirilir. Not: Bu özellik olarak ayarlanırsa içerik görüntüsünün doğruluğu etkilenebilir.`doğru` . Varsayılan`YANLIŞ` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Örnekler

XPS'e kaydederken belge nesnelerinin nasıl optimize edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Belgenin "Kaydet" yöntemine geçirilecek bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e nasıl dönüştüreceğini değiştirmek için.
XpsSaveOptions saveOptions = new XpsSaveOptions();
// İç içe geçmiş veya boş tuvalleri kaldırmak gibi önlemler almak için "OptimizeOutput" özelliğini "true" olarak ayarlayın
// ve çıktı belgesinin içeriğini optimize etmek için aynı biçimlendirmeye sahip bitişik çalışmaları birleştirmek.
// Bu, belgenin görünümünü etkileyebilir.
// Belgeyi normal şekilde kaydetmek için "OptimizeOutput" özelliğini "false" olarak ayarlayın.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Ayrıca bakınız

* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
