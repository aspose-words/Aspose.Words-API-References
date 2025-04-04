---
title: ImageSavingArgs.keepImageStreamOpen property
linktitle: keepImageStreamOpen property
articleTitle: keepImageStreamOpen property
second_title: Aspose.Words for Node.js
description: "ImageSavingArgs.keepImageStreamOpen property. Specifies whether Aspose.Words should keep the stream open or close it after saving an image."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/imagesavingargs/keepImageStreamOpen/
---

## ImageSavingArgs.keepImageStreamOpen property

Specifies whether Aspose.Words should keep the stream open or close it after saving an image.


```js
get keepImageStreamOpen(): boolean
```

### Remarks

Default is ``false`` and Aspose.Words will close the stream you provided
in the Aspose.Words.Saving.ImageSavingArgs.ImageStream property after writing an image into it.
Specify ``true`` to keep the stream open.




### Examples

Shows how to involve an image saving callback in an HTML conversion process.

```js
test.skip('ImageSavingCallback - TODO: imageSavingCallback not supported', () => {
    let doc = new aw.Document(base.myDir + "Rendering.docx");

    // When we save the document to HTML, we can pass a SaveOptions object to designate a callback
    // to customize the image saving process.
    let options = new aw.Saving.HtmlSaveOptions();
    options.imageSavingCallback = new ImageShapePrinter();

    doc.save(base.artifactsDir + "HtmlSaveOptions.imageSavingCallback.html", options);
  });

/*
    /// <summary>
    /// Prints the properties of each image as the saving process saves it to an image file in the local file system
    /// during the exporting of a document to HTML.
    /// </summary>
  private class ImageShapePrinter : IImageSavingCallback
  {
    void aw.Saving.IImageSavingCallback.imageSaving(ImageSavingArgs args)
    {
      args.keepImageStreamOpen = false;
      expect(args.isImageAvailable).toEqual(true);

      console.log(`${args.document.originalFileName.split('\\').Last()} Image #${++mImageCount}`);

      let layoutCollector = new aw.Layout.LayoutCollector(args.document);

      console.log(`\tOn page:\t${layoutCollector.getStartPageIndex(args.currentShape)}`);
      console.log(`\tDimensions:\t${args.currentShape.bounds}`);
      console.log(`\tAlignment:\t${args.currentShape.verticalAlignment}`);
      console.log(`\tWrap type:\t${args.currentShape.wrapType}`);
      console.log(`Output filename:\t${args.imageFileName}\n`);
    }

    private int mImageCount;
  }
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSavingArgs](../)

