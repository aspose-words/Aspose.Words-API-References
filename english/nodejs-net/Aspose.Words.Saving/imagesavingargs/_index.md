---
title: ImageSavingArgs class
linktitle: ImageSavingArgs class
articleTitle: ImageSavingArgs class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.ImageSavingArgs class. Provides data for the [IImageSavingCallback.imageSaving()](../iimagesavingcallback/imageSaving/#imagesavingargs) event"
type: docs
weight: 400
url: /nodejs-net/aspose.words.saving/imagesavingargs/
---

## ImageSavingArgs class

Provides data for the [IImageSavingCallback.imageSaving()](../iimagesavingcallback/imageSaving/#imagesavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Remarks

By default, when Aspose.Words saves a document to HTML, it saves each image into 
a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name
for each image found in the document.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to 
completely circumvent saving of images into files by providing your own stream objects.

To apply your own logic for generating image file names use the 
[ImageSavingArgs.imageFileName](./imageFileName/), [ImageSavingArgs.currentShape](./currentShape/) and [ImageSavingArgs.isImageAvailable](./isImageAvailable/) 
properties.

To save images into streams instead of files, use the Aspose.Words.Saving.ImageSavingArgs.ImageStream property.




### Properties

| Name | Description |
| --- | --- |
| [currentShape](./currentShape/) | Gets the [ShapeBase](../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape  that is about to be saved. |
| [document](./document/) | Gets the document object that is currently being saved. |
| [imageFileName](./imageFileName/) | Gets or sets the file name (without path) where the image will be saved to. |
| [isImageAvailable](./isImageAvailable/) | Returns ``true`` if the current image is available for export. |
| [keepImageStreamOpen](./keepImageStreamOpen/) | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |

### Examples

Shows how to split a document into parts and save them.

```js
test('DocumentPartsFileNames', () => {
  let doc = new aw.Document(base.myDir + "Rendering.docx");
  string outFileName = "SavingCallback.DocumentPartsFileNames.html";

  // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
  // to modify how we convert the document to HTML.
  let options = new aw.Saving.HtmlSaveOptions();

  // If we save the document normally, there will be one output HTML
  // document with all the source document's contents.
  // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
  // save our document to multiple HTML files: one for each section.
  options.documentSplitCriteria = aw.Saving.DocumentSplitCriteria.SectionBreak;

  // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
  options.documentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.documentSplitCriteria);

  // If we convert a document that contains images into html, we will end up with one html file which links to several images.
  // Each image will be in the form of a file in the local file system.
  // There is also a callback that can customize the name and file system location of each image.
  options.imageSavingCallback = new SavedImageRename(outFileName);

  doc.save(base.artifactsDir + outFileName, options);
});


  /// <summary>
  /// Sets custom filenames for output documents that the saving operation splits a document into.
  /// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
  public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
  {
    mOutFileName = outFileName;
    mDocumentSplitCriteria = documentSplitCriteria;
  }

  void aw.Saving.IDocumentPartSavingCallback.documentPartSaving(DocumentPartSavingArgs args)
  {
      // We can access the entire source document via the "Document" property.
    expect(args.document.originalFileName.EndsWith("Rendering.docx")).toEqual(true);

    string partType = '';

    switch (mDocumentSplitCriteria)
    {
      case aw.Saving.DocumentSplitCriteria.PageBreak:
        partType = "Page";
        break;
      case aw.Saving.DocumentSplitCriteria.ColumnBreak:
        partType = "Column";
        break;
      case aw.Saving.DocumentSplitCriteria.SectionBreak:
        partType = "Section";
        break;
      case aw.Saving.DocumentSplitCriteria.HeadingParagraph:
        partType = "Paragraph from heading";
        break;
    }

    string partFileName = `${mOutFileName} part ${++mCount}, of type ${partType}${Path.GetExtension(args.documentPartFileName)}`;

      // Below are two ways of specifying where Aspose.Words will save each part of the document.
      // 1 -  Set a filename for the output part file:
    args.documentPartFileName = partFileName;

      // 2 -  Create a custom stream for the output part file:
    args.documentPartStream = new FileStream(base.artifactsDir + partFileName, FileMode.create);

    expect(args.documentPartStream.CanWrite).toEqual(true);
    expect(args.keepDocumentPartStreamOpen).toEqual(false);
  }

  private int mCount;
  private readonly string mOutFileName;
  private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

  /// <summary>
  /// Sets custom filenames for image files that an HTML conversion creates.
  /// </summary>
public class SavedImageRename : IImageSavingCallback
{
  public SavedImageRename(string outFileName)
  {
    mOutFileName = outFileName;
  }

  void aw.Saving.IImageSavingCallback.imageSaving(ImageSavingArgs args)
  {
    string imageFileName = `${mOutFileName} shape ${++mCount}, of type ${args.currentShape.shapeType}${Path.GetExtension(args.imageFileName)}`;

      // Below are two ways of specifying where Aspose.Words will save each part of the document.
      // 1 -  Set a filename for the output image file:
    args.imageFileName = imageFileName;

      // 2 -  Create a custom stream for the output image file:
    args.imageStream = new FileStream(base.artifactsDir + imageFileName, FileMode.create);

    expect(args.imageStream.CanWrite).toEqual(true);
    expect(args.isImageAvailable).toEqual(true);
    expect(args.keepImageStreamOpen).toEqual(false);
  }

  private int mCount;
  private readonly string mOutFileName;
}
```

### See Also

* module [Aspose.Words.Saving](../)

