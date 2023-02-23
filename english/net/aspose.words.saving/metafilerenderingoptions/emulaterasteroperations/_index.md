---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
second_title: Aspose.Words for .NET API Reference
description: MetafileRenderingOptions property. Gets or sets a value determining whether or not the raster operations should be emulated in C#.
type: docs
weight: 30
url: /net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

Gets or sets a value determining whether or not the raster operations should be emulated.

```csharp
public bool EmulateRasterOperations { get; set; }
```

## Remarks

Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics. Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the metafile rendering performance.

When this value is set to `true`, Aspose.Words emulates the raster operations. The resulting output maybe partially rasterized and performance might be slower.

When this value is set to `false`, Aspose.Words does not emulate the raster operations. When Aspose.Words encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is `true`.

## Examples

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```csharp
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

* class [MetafileRenderingOptions](../)
* namespace [Aspose.Words.Saving](../../metafilerenderingoptions/)
* assembly [Aspose.Words](../../../)
