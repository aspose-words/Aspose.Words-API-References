---
title: IgnorePrinterMetrics
second_title: Aspose.Words per .NET API Reference
description: Ottiene o imposta lindicazione se lopzione di compatibilità Usa le metriche della stampante per il layout del documento è ignorata. Limpostazione predefinita è True.
type: docs
weight: 50
url: /it/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Ottiene o imposta l'indicazione se l'opzione di compatibilità "Usa le metriche della stampante per il layout del documento" è ignorata. L'impostazione predefinita è True.

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

### Esempi

Mostra come ignorare l'opzione "Usa le metriche della stampante per il layout del documento".

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Guarda anche

* class [LayoutOptions](../../layoutoptions)
* spazio dei nomi [Aspose.Words.Layout](../../layoutoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
