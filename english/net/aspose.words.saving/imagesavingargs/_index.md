---
title: ImageSavingArgs Class
linktitle: ImageSavingArgs
articleTitle: ImageSavingArgs
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.ImageSavingArgs class. Provides data for the ImageSaving event in C#.
type: docs
weight: 5190
url: /net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Provides data for the [`ImageSaving`](../iimagesavingcallback/imagesaving/) event.

To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.

```csharp
public class ImageSavingArgs
```

## Properties

| Name | Description |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Gets the [`ShapeBase`](../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape that is about to be saved. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Gets the document object that is currently being saved. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Gets or sets the file name (without path) where the image will be saved to. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Allows to specify the stream where the image will be saved to. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | Returns `true` if the current image is available for export. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Specifies whether Aspose.Words should keep the stream open or close it after saving an image. |

## Remarks

By default, when Aspose.Words saves a document to HTML, it saves each image into a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document.

`ImageSavingArgs` allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

To apply your own logic for generating image file names use the [`ImageFileName`](./imagefilename/), [`CurrentShape`](./currentshape/) and [`IsImageAvailable`](./isimageavailable/) properties.

To save images into streams instead of files, use the [`ImageStream`](./imagestream/) property.

## Examples

Shows how to split a document into parts and save them.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we convert the document to HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // If we save the document normally, there will be one output HTML
    // document with all the source document's contents.
    // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
    // save our document to multiple HTML files: one for each section.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // If we convert a document that contains images into html, we will end up with one html file which links to several images.
    // Each image will be in the form of a file in the local file system.
    // There is also a callback that can customize the name and file system location of each image.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

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

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // We can access the entire source document via the "Document" property.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Below are two ways of specifying where Aspose.Words will save each part of the document.
        // 1 -  Set a filename for the output part file:
        args.DocumentPartFileName = partFileName;

        // 2 -  Create a custom stream for the output part file:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
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

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Below are two ways of specifying where Aspose.Words will save each part of the document.
        // 1 -  Set a filename for the output image file:
        args.ImageFileName = imageFileName;

        // 2 -  Create a custom stream for the output image file:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
