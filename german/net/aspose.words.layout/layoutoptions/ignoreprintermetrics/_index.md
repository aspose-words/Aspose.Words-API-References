---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words für .NET
description: LayoutOptions IgnorePrinterMetrics eigendom. Ruft die Angabe ab ob die Kompatibilitätsoption Druckermetriken zum Layouten des Dokuments verwenden ignoriert wird oder legt diese fest. Standard istWAHR  in C#.
type: docs
weight: 50
url: /de/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Ruft die Angabe ab, ob die Kompatibilitätsoption „Druckermetriken zum Layouten des Dokuments verwenden“ ignoriert wird, oder legt diese fest. Standard ist`WAHR` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Beispiele

Zeigt, wie die Option „Druckermetriken zum Layouten des Dokuments verwenden“ ignoriert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Siehe auch

* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
