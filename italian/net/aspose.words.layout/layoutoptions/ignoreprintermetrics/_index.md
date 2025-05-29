---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words per .NET
description: Scopri la proprietà IgnorePrinterMetrics di LayoutOptions, controlla le metriche di stampa per il layout del documento. Ottimizza la compatibilità e migliora la precisione di stampa.
type: docs
weight: 50
url: /it/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Ottiene o imposta l'indicazione se l'opzione di compatibilità "Usa le metriche della stampante per disporre il documento" viene ignorata. Il valore predefinito è`VERO` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Esempi

Mostra come ignorare l'opzione "Usa le metriche della stampante per disporre il documento".

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Guarda anche

* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
