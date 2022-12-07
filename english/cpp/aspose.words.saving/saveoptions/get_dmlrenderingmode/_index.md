---
title: get_DmlRenderingMode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining how DrawingML shapes are rendered.
type: docs
weight: 92
url: /cpp/aspose.words.saving/saveoptions/get_dmlrenderingmode/
---
## SaveOptions::get_DmlRenderingMode method


Gets or sets a value determining how DrawingML shapes are rendered.

```cpp
Aspose::Words::Saving::DmlRenderingMode Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode() const
```

## Remarks


The default value is [Fallback](../../dmlrenderingmode/).

This property is used when the document is exported to fixed page formats.

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

* Enum [DmlRenderingMode](../../dmlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
