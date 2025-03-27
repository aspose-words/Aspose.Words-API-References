---
title: MetafileRenderingOptions class
linktitle: MetafileRenderingOptions class
articleTitle: MetafileRenderingOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.MetafileRenderingOptions class. Allows to specify additional metafile rendering options"
type: docs
weight: 480
url: /nodejs-net/Aspose.Words.Saving/metafilerenderingoptions/
---

## MetafileRenderingOptions class

Allows to specify additional metafile rendering options.
To learn more, visit the [Handling Windows Metafiles](https://docs.aspose.com/words/nodejs-net/handling-windows-metafiles/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [MetafileRenderingOptions()](./MetafileRenderingOptions/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [emfPlusDualRenderingMode](./emfPlusDualRenderingMode/) | Gets or sets a value determining how EMF+ Dual metafiles should be rendered. |
| [emulateRasterOperations](./emulateRasterOperations/) | Gets or sets a value determining whether or not the raster operations should be emulated. |
| [emulateRenderingToSizeOnPage](./emulateRenderingToSizeOnPage/) | Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size. |
| [emulateRenderingToSizeOnPageResolution](./emulateRenderingToSizeOnPageResolution/) | Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page. |
| [renderingMode](./renderingMode/) | Gets or sets a value determining how metafile images should be rendered. |
| [useEmfEmbeddedToWmf](./useEmfEmbeddedToWmf/) | Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered. |
| [useGdiRasterOperationsEmulation](./useGdiRasterOperationsEmulation/) | Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation. |

### Examples

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```js
test.skip('HandleBinaryRasterWarnings - TODO: WORDSNODEJS-108 - Add support of IWarningCallback', () => {
    let doc = new aw.Document(base.myDir + "WMF with image.docx");

    let metafileRenderingOptions = new aw.Saving.MetafileRenderingOptions();

    // Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
    // it encounters a metafile, which will require raster operations to render in the output PDF.
    metafileRenderingOptions.emulateRasterOperations = false;

    // Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
    metafileRenderingOptions.renderingMode = aw.Saving.MetafileRenderingMode.VectorWithFallback;

    // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
    // to modify how that method converts the document to .PDF and applies the configuration
    // in our MetafileRenderingOptions object to the saving operation.
    let saveOptions = new aw.Saving.PdfSaveOptions();
    saveOptions.metafileRenderingOptions = metafileRenderingOptions;

    let callback = new HandleDocumentWarnings();
    doc.warningCallback = callback;

    doc.save(base.artifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    expect(callback.Warnings.count).toEqual(1);
    expect(callback.Warnings.at(0).description).toEqual("'R2_XORPEN' binary raster operation is not supported.");
  });

/*
    /// <summary>
    /// Prints and collects formatting loss-related warnings that occur upon saving a document.
    /// </summary>
  public class HandleDocumentWarnings : IWarningCallback
  {
    public void Warning(WarningInfo info)
    {
      if (info.warningType == aw.WarningType.MinorFormattingLoss)
      {
        console.log("Unsupported operation: " + info.description);
        Warnings.warning(info);
      }
    }

    public WarningInfoCollection Warnings = new aw.WarningInfoCollection();
  }
```

### See Also

* module [Aspose.Words.Saving](../)

