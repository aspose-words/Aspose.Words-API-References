---
title: DmlEffectsRenderingMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how DrawingML effects are rendered to fixed page formats.
type: docs
weight: 638
url: /cpp/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enum


Specifies how DrawingML effects are rendered to fixed page formats.

```cpp
enum class DmlEffectsRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Simplified | 0 | [Rendering](../../aspose.words.rendering/) of DrawingML effects are simplified. |
| None | 1 | No DrawingML effects are rendered. |
| Fine | 2 | DrawingML effects are rendered in fine mode which involves advanced processing. In this mode rendering of effects gives better results but at a higher performance cost than [Simplified](./) mode. |


## Examples



Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"DrawingML shape effects.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
// to render a simplified version of DrawingML effects.
// Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
// render DrawingML effects with more accuracy and also with more processing cost.
options->set_DmlEffectsRenderingMode(effectsRenderingMode);

ASSERT_EQ(DmlRenderingMode::DrawingML, options->get_DmlRenderingMode());

doc->Save(ArtifactsDir + u"PdfSaveOptions.DrawingMLEffects.pdf", options);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
