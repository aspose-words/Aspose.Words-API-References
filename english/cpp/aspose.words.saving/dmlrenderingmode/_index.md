---
title: DmlRenderingMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how DrawingML shapes are rendered to fixed page formats.
type: docs
weight: 651
url: /cpp/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enum


Specifies how DrawingML shapes are rendered to fixed page formats.

```cpp
enum class DmlRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Fallback | 0 | If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. |
| DrawingML | 1 | Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. This is the default mode. |


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


Shows how to render fallback shapes when saving to PDF. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"DrawingML shape fallbacks.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
// to substitute DML shapes with their fallback shapes.
// Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
// to render the DML shapes themselves.
options->set_DmlRenderingMode(dmlRenderingMode);

doc->Save(ArtifactsDir + u"PdfSaveOptions.DrawingMLFallback.pdf", options);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
