---
title: IgnorePrinterMetrics
second_title: Aspose.Words for .NET API Reference
description: LayoutOptions property. Gets or sets indication of whether the Use printer metrics to lay out document compatibility option is ignored. Default is true in C#.
type: docs
weight: 50
url: /net/aspose.words.layout/layoutoptions/ignoreprintermetrics/
---
## LayoutOptions.IgnorePrinterMetrics property

Gets or sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is `true`.

```csharp
public bool IgnorePrinterMetrics { get; set; }
```

## Examples

Shows how to ignore 'Use printer metrics to lay out document' option.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

doc.LayoutOptions.IgnorePrinterMetrics = false;

doc.Save(ArtifactsDir + "Document.IgnorePrinterMetrics.docx");
```

### See Also

* class [LayoutOptions](../)
* namespace [Aspose.Words.Layout](../../layoutoptions/)
* assembly [Aspose.Words](../../../)
