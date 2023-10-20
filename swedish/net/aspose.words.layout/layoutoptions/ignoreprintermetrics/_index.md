---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words för .NET
description: LayoutOptions IgnorePrinterMetrics fast egendom. Hämtar eller ställer in en indikation på om kompatibilitetsalternativet Använd skrivarmått för att lägga ut dokument ignoreras. Standard ärSann  i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Hämtar eller ställer in en indikation på om kompatibilitetsalternativet "Använd skrivarmått för att lägga ut dokument" ignoreras. Standard är`Sann` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Exempel

Visar hur man ignorerar alternativet "Använd skrivarmått för att lägga upp dokument".

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Se även

* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
