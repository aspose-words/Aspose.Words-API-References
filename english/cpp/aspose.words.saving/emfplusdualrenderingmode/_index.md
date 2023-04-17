---
title: Aspose::Words::Saving::EmfPlusDualRenderingMode enum
linktitle: EmfPlusDualRenderingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::EmfPlusDualRenderingMode enum. Specifies how Aspose.Words should render EMF+ Dual metafiles in C++.'
type: docs
weight: 53000
url: /cpp/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enum


Specifies how Aspose.Words should render EMF+ Dual metafiles.

```cpp
enum class EmfPlusDualRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| EmfPlusWithFallback | 0 | Aspose.Words tries to render EMF+ part of EMF+ Dual metafile. If some of the EMF+ records are not supported then Aspose.Words renders EMF part of EMF+ Dual metafile. |
| EmfPlus | 1 | Aspose.Words renders EMF+ part of EMF+ Dual metafile. |
| Emf | 2 | Aspose.Words renders EMF part of EMF+ Dual metafile. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
