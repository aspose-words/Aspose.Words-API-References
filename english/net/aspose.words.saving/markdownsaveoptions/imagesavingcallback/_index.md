---
title: MarkdownSaveOptions.ImageSavingCallback
linktitle: ImageSavingCallback
articleTitle: ImageSavingCallback
second_title: Aspose.Words for .NET
description: Control image saving in Markdown with MarkdownSaveOptions' ImageSavingCallback. Enhance document formatting and streamline your workflow effortlessly!
type: docs
weight: 70
url: /net/aspose.words.saving/markdownsaveoptions/imagesavingcallback/
---
## MarkdownSaveOptions.ImageSavingCallback property

Allows to control how images are saved when a document is saved to Markdown format.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

## Examples

Shows how to rename the image name during saving into Markdown document.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
    // Each image will be in the form of a file in the local file system.
    // There is also a callback that can customize the name and file system location of each image.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // The ImageSaving() method of our callback will be run at this time.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.That(Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")), Is.EqualTo(1));
    Assert.That(Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")), Is.EqualTo(8));
}

/// <summary>
/// Renames saved images that are produced when an Markdown document is saved.
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

        args.ImageFileName = imageFileName;
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.That(args.ImageStream.CanWrite, Is.True);
        Assert.That(args.IsImageAvailable, Is.True);
        Assert.That(args.KeepImageStreamOpen, Is.False);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### See Also

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
