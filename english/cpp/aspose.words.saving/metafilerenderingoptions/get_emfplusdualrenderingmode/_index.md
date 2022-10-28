---
title: get_EmfPlusDualRenderingMode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining how EMF+ Dual metafiles should be rendered.
type: docs
weight: 14
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions.get_EmfPlusDualRenderingMode method


Gets or sets a value determining how EMF+ Dual metafiles should be rendered.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```


EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part. Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, EMF+ part is always used.

The default value is **EmfPlusWithFallback**.

## Examples




Shows how to configure Enhanced Windows Metafile-related rendering options when saving to PDF. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"EMF.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();

// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.Emf"
// to only render the EMF part of an EMF+ dual metafile.
// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlus" to
// to render the EMF+ part of an EMF+ dual metafile.
// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// to render the EMF+ part of an EMF+ dual metafile if all of the EMF+ records are supported.
// Otherwise, Aspose.Words will render the EMF part.
saveOptions->get_MetafileRenderingOptions()->set_EmfPlusDualRenderingMode(renderingMode);

// Set the "UseEmfEmbeddedToWmf" property to "true" to render embedded EMF data
// for metafiles that we can render as vector graphics.
saveOptions->get_MetafileRenderingOptions()->set_UseEmfEmbeddedToWmf(true);

doc->Save(ArtifactsDir + u"PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

