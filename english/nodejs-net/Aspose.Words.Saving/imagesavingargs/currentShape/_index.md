---
title: ImageSavingArgs.currentShape property
linktitle: currentShape property
articleTitle: currentShape property
second_title: Aspose.Words for NodeJs
description: "ImageSavingArgs.currentShape property. Gets the [ShapeBase](../../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape  that is about to be saved."
type: docs
weight: 10
url: /nodejs-net/aspose.words.saving/imagesavingargs/currentShape/
---

## ImageSavingArgs.currentShape property

Gets the [ShapeBase](../../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape 
that is about to be saved.



```js
get currentShape(): Aspose.Words.Drawing.ShapeBase
```

### Remarks

[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. 
That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing 
[ShapeBase.shapeType](../../../aspose.words.drawing/shapebase/shapeType/) with [ShapeType.Group](../../../aspose.words.drawing/shapetype/#Group) or by casting it to one of derived classes: 
[Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words uses the document file name and a unique number to generate unique file name 
for each image found in the document. You can use the [ImageSavingArgs.currentShape](./) property to generate 
a "better" file name by examining shape properties such as [ImageData.title](../../../aspose.words.drawing/imagedata/title/) 
(Shape only), [ImageData.sourceFullName](../../../aspose.words.drawing/imagedata/sourceFullName/) (Shape only) 
and [ShapeBase.name](../../../aspose.words.drawing/shapebase/name/). Of course you can build file names using any other properties or criteria 
but note that subsidiary file names must be unique within the export operation.

Some images in the document can be unavailable. To check image availability 
use the [ImageSavingArgs.isImageAvailable](../isImageAvailable/) property.




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

