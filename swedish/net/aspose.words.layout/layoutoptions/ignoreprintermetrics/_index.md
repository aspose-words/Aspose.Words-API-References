---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LayoutOptions IgnorePrinterMetrics, styr skrivarmätvärden för dokumentlayout. Optimera kompatibilitet och förbättra utskriftsprecisionen.
type: docs
weight: 50
url: /sv/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Hämtar eller anger om kompatibilitetsalternativet "Använd skrivarmått för att utforma dokument" ignoreras. Standard är`sann` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Exempel

Visar hur man ignorerar alternativet "Använd skrivarmått för att utforma dokumentet".

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Se även

* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
