---
title: get_DmlEffectsRenderingMode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining how DrawingML effects are rendered.
type: docs
weight: 118
url: /cpp/aspose.words.saving/pdfsaveoptions/get_dmleffectsrenderingmode/
---
## PdfSaveOptions.get_DmlEffectsRenderingMode method


Gets or sets a value determining how DrawingML effects are rendered.

```cpp
Aspose::Words::Saving::DmlEffectsRenderingMode Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode() override
```


The default value is **Simplified**.

This property is used when the document is exported to fixed page formats.

If [Compliance](../get_compliance/) is set to **PdfA1a** or **PdfA1b**, property always returns **None**.

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

