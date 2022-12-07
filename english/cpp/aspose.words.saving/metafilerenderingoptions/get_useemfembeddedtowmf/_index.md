---
title: get_UseEmfEmbeddedToWmf
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.
type: docs
weight: 79
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## Remarks


WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data. GDI+ always uses WMF data.

When this value is set to **true**, Aspose.Words uses embedded EMF data when rendering.

When this value is set to **false**, Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, WMF data is always used.

The default value is **true**.

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

## See Also

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
