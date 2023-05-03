---
title: FixedPageSaveOptions.PageSavingCallback
linktitle: PageSavingCallback
second_title: Aspose.Words for .NET API Reference
description: FixedPageSaveOptions PageSavingCallback property. Allows to control how separate pages are saved when a document is exported to fixed page format in C#.
type: docs
weight: 60
url: /net/aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/
---
## PageSavingCallback property

Allows to control how separate pages are saved when a document is exported to fixed page format.

```csharp
public IPageSavingCallback PageSavingCallback { get; set; }
```

## Examples

Shows how to use a callback to save a document to HTML page by page.

```csharp
public void PageFileNames()
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

* interface [IPageSavingCallback](../../ipagesavingcallback/)
* class [FixedPageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* assembly [Aspose.Words](../../../)
