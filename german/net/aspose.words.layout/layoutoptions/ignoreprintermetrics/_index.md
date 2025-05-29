---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „LayoutOptions IgnorePrinterMetrics“ und steuern Sie die Druckermetriken für das Dokumentlayout. Optimieren Sie die Kompatibilität und verbessern Sie die Druckpräzision.
type: docs
weight: 50
url: /de/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Ruft ab oder legt fest, ob die Kompatibilitätsoption „Druckermaße zum Layouten von Dokumenten verwenden“ ignoriert wird. Der Standardwert ist`WAHR` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Beispiele

Zeigt, wie die Option „Druckermaße zum Layouten des Dokuments verwenden“ ignoriert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Siehe auch

* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
