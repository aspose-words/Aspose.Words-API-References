---
title: Enum DmlEffectsRenderingMode
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Saving.DmlEffectsRenderingMode enum. Specifies how DrawingML effects are rendered to fixed page formats in C#.
type: docs
weight: 4690
url: /net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

Specifies how DrawingML effects are rendered to fixed page formats.

```csharp
public enum DmlEffectsRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Simplified | `0` | Rendering of DrawingML effects are simplified. |
| None | `1` | No DrawingML effects are rendered. |
| Fine | `2` | DrawingML effects are rendered in fine mode which involves advanced processing. In this mode rendering of effects gives better results but at a higher performance cost than Simplified mode. |

## Examples

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
