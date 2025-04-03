---
title: DocumentPartSavingArgs.documentPartFileName property
linktitle: documentPartFileName property
articleTitle: documentPartFileName property
second_title: Aspose.Words for NodeJs
description: "DocumentPartSavingArgs.documentPartFileName property. Gets or sets the file name (without path) where the document part will be saved to."
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/documentpartsavingargs/documentPartFileName/
---

## DocumentPartSavingArgs.documentPartFileName property

Gets or sets the file name (without path) where the document part will be saved to.


```js
get documentPartFileName(): string
```

### Remarks

This property allows you to redefine how the document part file names are generated
during export to HTML or EPUB.

When the callback is invoked, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the document part into a 
different file. Note that the file name for each part must be unique.

[DocumentPartSavingArgs.documentPartFileName](./) must contain only the file name without the path. 
Aspose.Words determines the path for saving using the document file name. If output document 
file name was not specified, for instance when saving to a stream, this file name is used only 
for referencing document parts. The same is true when saving to EPUB format.




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

* module [Aspose.Words.Saving](../../)
* class [DocumentPartSavingArgs](../)

