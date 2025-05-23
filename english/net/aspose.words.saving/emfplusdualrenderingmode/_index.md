---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET
description: Discover Aspose.Words' EMF Plus Dual Rendering Mode enum for optimal EMF Dual metafile rendering. Enhance your document processing with precision!
type: docs
weight: 5730
url: /net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Specifies how Aspose.Words should render EMF+ Dual metafiles.

```csharp
public enum EmfPlusDualRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words tries to render EMF+ part of EMF+ Dual metafile. If some of the EMF+ records are not supported then Aspose.Words renders EMF part of EMF+ Dual metafile. |
| EmfPlus | `1` | Aspose.Words renders EMF+ part of EMF+ Dual metafile. |
| Emf | `2` | Aspose.Words renders EMF part of EMF+ Dual metafile. |

## Examples

Shows how to configure Enhanced Windows Metafile-related rendering options when saving to PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.Emf"
// to only render the EMF part of an EMF+ dual metafile.
// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlus" to
// to render the EMF+ part of an EMF+ dual metafile.
// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// to render the EMF+ part of an EMF+ dual metafile if all of the EMF+ records are supported.
// Otherwise, Aspose.Words will render the EMF part.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Set the "UseEmfEmbeddedToWmf" property to "true" to render embedded EMF data
// for metafiles that we can render as vector graphics.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
