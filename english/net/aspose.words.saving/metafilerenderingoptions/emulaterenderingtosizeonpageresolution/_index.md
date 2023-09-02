---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words for .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution property. Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page in C#.
type: docs
weight: 50
url: /net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Remarks

This option is used only when [`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) is set to `true`.

The default value is 96. This is a default display resolution. I.e. metafile rendering will emulate the display of the metafile in MS Word with a 100% zoom factor.

## Examples

Shows how to display of the metafile according to the size on page.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Set the "EmulateRenderingToSizeOnPage" property to "true"
// to emulate rendering according to the metafile size on page.
// Set the "EmulateRenderingToSizeOnPage" property to "false"
// to emulate metafile rendering to its default size in pixels.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### See Also

* class [MetafileRenderingOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
