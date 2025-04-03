---
title: IWarningCallback class
linktitle: IWarningCallback class
articleTitle: IWarningCallback class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.IWarningCallback class. Implement this interface if you want to have your own custom method called to  capture loss of fidelity warnings that can occur during document loading or saving."
type: docs
weight: 600
url: /nodejs-net/aspose.words/iwarningcallback/
---

## IWarningCallback class

Implement this interface if you want to have your own custom method called to 
capture loss of fidelity warnings that can occur during document loading or saving.


### Methods

| Name | Description |
| --- | --- |
|[ warning(info)](./warning/#warninginfo) | Aspose.Words invokes this method when it encounters some issue during document loading  or saving that might result in loss of formatting or data fidelity. |

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

* module [Aspose.Words](../)

