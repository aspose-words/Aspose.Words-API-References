---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words for .NET
description: Discover how Aspose.Words.Saving.DmlRenderingMode enhances DrawingML shape rendering for high-quality fixed page formats. Optimize your document visuals!
type: docs
weight: 5530
url: /net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

Specifies how DrawingML shapes are rendered to fixed page formats.

```csharp
public enum DmlRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Fallback | `0` | If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. |
| DrawingML | `1` | Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. This is the default mode. |

## Examples

Shows how to render fallback shapes when saving to PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
// to substitute DML shapes with their fallback shapes.
// Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
// to render the DML shapes themselves.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
// to render a simplified version of DrawingML effects.
// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
// render DrawingML effects with more accuracy and also with more processing cost.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
