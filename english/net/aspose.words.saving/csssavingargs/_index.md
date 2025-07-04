---
title: CssSavingArgs Class
linktitle: CssSavingArgs
articleTitle: CssSavingArgs
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.CssSavingArgs class, designed to enhance your document processing with customizable CssSaving event data for optimal results.
type: docs
weight: 5610
url: /net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Provides data for the [`CssSaving`](../icsssavingcallback/csssaving/) event.

To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.

```csharp
public class CssSavingArgs
```

## Properties

| Name | Description |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | Allows to specify the stream where the CSS information will be saved to. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Gets the document object that is currently being saved. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is `true`. When this property is `false`, the CSS information will not be saved to a CSS file and will not be embedded to HTML document. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information. |

## Remarks

By default, when Aspose.Words saves a document to HTML, it saves CSS information inline (as a value of the **style** attribute on every element).

`CssSavingArgs` allows to save CSS information into file by providing your own stream object.

To save CSS into stream, use the [`CssStream`](./cssstream/) property.

To suppress saving CSS into a file and embedding to HTML document use the [`IsExportNeeded`](./isexportneeded/) property.

## Examples

Shows how to work with CSS stylesheets that an HTML conversion creates.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we convert the document to HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
    // accompany a saved HTML document with an external CSS stylesheet file.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Below are two ways of specifying directories and filenames for output CSS stylesheets.
    // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 -  Use a custom callback to name our stylesheet:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Sets a custom filename, along with other parameters for an external CSS stylesheet.
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        // We can access the entire source document via the "Document" property.
        Assert.That(args.Document.OriginalFileName.EndsWith("Rendering.docx"), Is.True);

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.That(args.CssStream.CanWrite, Is.True);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
