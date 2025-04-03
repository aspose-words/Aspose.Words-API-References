---
title: MetafileRenderingMode enumeration
linktitle: MetafileRenderingMode enumeration
articleTitle: MetafileRenderingMode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.MetafileRenderingMode enumeration. Specifies how Aspose.Words should render WMF and EMF metafiles."
type: docs
weight: 470
url: /nodejs-net/aspose.words.saving/metafilerenderingmode/
---

## MetafileRenderingMode enumeration

Specifies how Aspose.Words should render WMF and EMF metafiles.


### Members

| Name | Description |
| --- | --- |
| VectorWithFallback | Aspose.Words tries to render a metafile as vector graphics. If Aspose.Words cannot correctly render some of  the metafile records to vector graphics then Aspose.Words renders this metafile to a bitmap. |
| Vector | Aspose.Words renders a metafile as vector graphics. |
| Bitmap | Aspose.Words invokes GDI+ to render a metafile to a bitmap and then saves the bitmap to the output document. |

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

