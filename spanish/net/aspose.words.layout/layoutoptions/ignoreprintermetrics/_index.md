---
title: LayoutOptions.IgnorePrinterMetrics
linktitle: IgnorePrinterMetrics
articleTitle: IgnorePrinterMetrics
second_title: Aspose.Words para .NET
description: Descubra la propiedad IgnorePrinterMetrics de LayoutOptions, que controla las métricas de la impresora para el diseño del documento. Optimice la compatibilidad y mejore la precisión de la impresión.
type: docs
weight: 50
url: /es/net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Obtiene o establece la indicación de si se ignora la opción de compatibilidad "Usar métricas de impresora para diseñar el documento". El valor predeterminado es`verdadero` .

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Ejemplos

Muestra cómo ignorar la opción 'Usar métricas de impresora para diseñar el documento'.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### Ver también

* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
