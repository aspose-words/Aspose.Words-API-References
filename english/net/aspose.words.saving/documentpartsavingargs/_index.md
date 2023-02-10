---
title: Class DocumentPartSavingArgs
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Saving.DocumentPartSavingArgs class. Provides data for the DocumentPartSaving callback in C#.
type: docs
weight: 4720
url: /net/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class

Provides data for the [`DocumentPartSaving`](../idocumentpartsavingcallback/documentpartsaving/) callback.

To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.

```csharp
public class DocumentPartSavingArgs
```

## Properties

| Name | Description |
| --- | --- |
| [Document](../../aspose.words.saving/documentpartsavingargs/document/) { get; } | Gets the document object that is being saved. |
| [DocumentPartFileName](../../aspose.words.saving/documentpartsavingargs/documentpartfilename/) { get; set; } | Gets or sets the file name (without path) where the document part will be saved to. |
| [DocumentPartStream](../../aspose.words.saving/documentpartsavingargs/documentpartstream/) { get; set; } | Allows to specify the stream where the document part will be saved to. |
| [KeepDocumentPartStreamOpen](../../aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/) { get; set; } | Specifies whether Aspose.Words should keep the stream open or close it after saving a document part. |

## Remarks

When Aspose.Words saves a document to HTML or related formats and [`DocumentSplitCriteria`](../htmlsaveoptions/documentsplitcriteria/) is specified, the document is split into parts and by default, each document part is saved into a separate file.

Class `DocumentPartSavingArgs` allows you to control how each document part will be saved. It allows to redefine how file names are generated or to completely circumvent saving of document parts into files by providing your own stream objects.

To save document parts into streams instead of files, use the [`DocumentPartStream`](./documentpartstream/) property.

## Examples

Shows how to split a document into parts and save them.

```csharp
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
