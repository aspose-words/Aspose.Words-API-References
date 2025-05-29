---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: .NET için Aspose.Words
description: LayoutOptions IgnorePrinterMetrics özelliğini keşfedin, belge düzeni için yazıcı ölçümlerini kontrol edin. Uyumluluğu iyileştirin ve yazdırma hassasiyetini artırın.
type: docs
weight: 50
url: /tr/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

"Belgeyi düzenlemek için yazıcı ölçümlerini kullan" uyumluluk seçeneğinin göz ardı edilip edilmediğine ilişkin göstergeyi alır veya ayarlar. Varsayılan`doğru` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Örnekler

'Belgeyi düzenlemek için yazıcı ölçütlerini kullan' seçeneğinin nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Ayrıca bakınız

* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
