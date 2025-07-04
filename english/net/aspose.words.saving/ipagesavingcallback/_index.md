---
title: IPageSavingCallback Interface
linktitle: IPageSavingCallback
articleTitle: IPageSavingCallback
second_title: Aspose.Words for .NET
description: Control document saving with Aspose.Words.Saving.IPageSavingCallback. Customize how pages are saved in fixed formats for optimal results.
type: docs
weight: 5920
url: /net/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface

Implement this interface if you want to control how Aspose.Words saves separate pages when saving a document to fixed page formats.

```csharp
public interface IPageSavingCallback
```

## Methods

| Name | Description |
| --- | --- |
| [PageSaving](../../aspose.words.saving/ipagesavingcallback/pagesaving/)(*[PageSavingArgs](../pagesavingargs/)*) | Called when Aspose.Words saves a separate page to fixed page formats. |

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

    Assert.That(filePaths.Length, Is.EqualTo(3));
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

        Assert.That(args.KeepPageStreamOpen, Is.False);
    }
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
