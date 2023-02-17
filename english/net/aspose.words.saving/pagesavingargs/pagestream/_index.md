---
title: PageSavingArgs.PageStream
second_title: Aspose.Words for .NET API Reference
description: PageSavingArgs property. Allows to specify the stream where the document page will be saved to in C#.
type: docs
weight: 50
url: /net/aspose.words.saving/pagesavingargs/pagestream/
---
## PageSavingArgs.PageStream property

Allows to specify the stream where the document page will be saved to.

```csharp
public Stream PageStream { get; set; }
```

## Remarks

This property allows you to save document pages to streams instead of files.

The default value is `null`. When this property is `null`, the document page will be saved to a file specified in the [`PageFileName`](../pagefilename/) property.

If both `PageStream` and [`PageFileName`](../pagefilename/) are set, then PageStream will be used.

## Examples

Shows how to use a callback to save a document to HTML page by page.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we convert the document to HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // We will save each page in this document to a separate HTML file in the local file system.
    // Set a callback that allows us to name each output HTML document.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Saves all pages to a file and directory specified within.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Below are two ways of specifying where Aspose.Words will save each page of the document.
        // 1 -  Set a filename for the output page file:
        args.PageFileName = outFileName;

        // 2 -  Create a custom stream for the output page file:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### See Also

* class [PageSavingArgs](../)
* namespace [Aspose.Words.Saving](../../pagesavingargs/)
* assembly [Aspose.Words](../../../)
