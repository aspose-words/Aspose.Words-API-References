---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words for .NET
description: Discover how the EmulateRenderingToSizeOnPage property enhances metafile rendering, ensuring accurate display sizes for optimal visual results.
type: docs
weight: 40
url: /net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Remarks

When metafiles are displayed in MS Word, some graphics may be scaled according to the actual metafile size in pixels. I.e. even zooming may affect the metafile display.

When this value is set to `true`, Aspose.Words emulates rendering according to the metafile size on page. The size in pixels is calculated from the metafile size on the page and the specified [`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

When this value is set to `false`, Aspose.Words emulates metafile rendering to its default size in pixels.

This option is used only when metafile is rendered as vector graphics.

The default value is `true`.

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
