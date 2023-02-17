---
title: CssSavingArgs.IsExportNeeded
second_title: Aspose.Words for .NET API Reference
description: CssSavingArgs property. Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is true. When this property is false the CSS information will not be saved to a CSS file and will not be embedded to HTML document in C#.
type: docs
weight: 30
url: /net/aspose.words.saving/csssavingargs/isexportneeded/
---
## CssSavingArgs.IsExportNeeded property

Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is `true`. When this property is `false`, the CSS information will not be saved to a CSS file and will not be embedded to HTML document.

```csharp
public bool IsExportNeeded { get; set; }
```

## Examples

Shows how to work with CSS stylesheets that an HTML conversion creates.

```csharp
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
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### See Also

* class [CssSavingArgs](../)
* namespace [Aspose.Words.Saving](../../csssavingargs/)
* assembly [Aspose.Words](../../../)
