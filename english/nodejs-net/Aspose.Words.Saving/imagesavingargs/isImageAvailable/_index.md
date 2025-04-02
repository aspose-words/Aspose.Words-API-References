---
title: ImageSavingArgs.isImageAvailable property
linktitle: isImageAvailable property
articleTitle: isImageAvailable property
second_title: Aspose.Words for NodeJs
description: "ImageSavingArgs.isImageAvailable property. Returns ``True`` if the current image is available for export."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/imagesavingargs/isImageAvailable/
---

## ImageSavingArgs.isImageAvailable property

Returns ``True`` if the current image is available for export.



```js
get isImageAvailable(): boolean
```

### Remarks

Some images in the document can be unavailable, for example, because the image
is linked and the link is inaccessible or does not point to a valid image. 
In this case Aspose.Words exports an icon with a red cross. This property returns 
``True`` if the original image is available; returns ``False`` if the original 
image is not available and a "no image" icon will be offered for save.

When saving a group shape or a shape that doesn't require any image this property 
is always ``True``.




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
* property [ImageSavingArgs.currentShape](../currentShape/)

