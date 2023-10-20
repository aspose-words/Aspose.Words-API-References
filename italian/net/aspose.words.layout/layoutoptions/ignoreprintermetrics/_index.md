---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words per .NET
description: LayoutOptions IgnorePrinterMetrics proprietà. Ottiene o imposta lindicazione se lopzione di compatibilità Utilizza parametri stampante per impaginare il documento viene ignorata. Limpostazione predefinita èVERO  in C#.
type: docs
weight: 50
url: /it/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Ottiene o imposta l'indicazione se l'opzione di compatibilità "Utilizza parametri stampante per impaginare il documento" viene ignorata. L'impostazione predefinita è`VERO` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Esempi

Mostra come ignorare l'opzione "Utilizza parametri stampante per impaginare il documento".

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Guarda anche

* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
