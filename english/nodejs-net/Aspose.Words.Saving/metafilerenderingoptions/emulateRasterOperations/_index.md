---
title: MetafileRenderingOptions.emulateRasterOperations property
linktitle: emulateRasterOperations property
articleTitle: emulateRasterOperations property
second_title: Aspose.Words for NodeJs
description: "MetafileRenderingOptions.emulateRasterOperations property. Gets or sets a value determining whether or not the raster operations should be emulated."
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/metafilerenderingoptions/emulateRasterOperations/
---

## MetafileRenderingOptions.emulateRasterOperations property

Gets or sets a value determining whether or not the raster operations should be emulated.


```js
get emulateRasterOperations(): boolean
```

### Remarks

Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics.
Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the
metafile rendering performance.

When this value is set to ``true``, Aspose.Words emulates the raster operations. The resulting output maybe
partially rasterized and performance might be slower.

When this value is set to ``false``, Aspose.Words does not emulate the raster operations. When Aspose.Words
encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the
operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is ``true``.




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

* module [Aspose.Words.Saving](../../)
* class [MetafileRenderingOptions](../)

