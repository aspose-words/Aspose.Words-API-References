---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.MetafileRenderingOptions class. Allows to specify additional metafile rendering options in C#.
type: docs
weight: 5250
url: /net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

Allows to specify additional metafile rendering options.

To learn more, visit the [Handling Windows Metafiles](https://docs.aspose.com/words/net/handling-windows-metafiles/) documentation article.

```csharp
public class MetafileRenderingOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | Gets or sets a value determining how EMF+ Dual metafiles should be rendered. |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | Gets or sets a value determining whether or not the raster operations should be emulated. |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | Gets or sets a value determining how metafile images should be rendered. |
| [ScaleWmfFontsToMetafileSize](../../aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/) { get; set; } | Gets or sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page. |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered. |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation. |

## Examples

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
    // it encounters a metafile, which will require raster operations to render in the output PDF.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
    // to modify how that method converts the document to .PDF and applies the configuration
    // in our MetafileRenderingOptions object to the saving operation.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is partly supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Prints and collects formatting loss-related warnings that occur upon saving a document.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
