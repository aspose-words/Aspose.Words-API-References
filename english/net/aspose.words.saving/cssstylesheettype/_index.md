---
title: CssStyleSheetType Enum
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.CssStyleSheetType enum. Specifies how CSS Cascading Style Sheet styles are exported to HTML in C#.
type: docs
weight: 4860
url: /net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

Specifies how CSS (Cascading Style Sheet) styles are exported to HTML.

```csharp
public enum CssStyleSheetType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Inline | `0` | CSS styles are written inline (as a value of the **style** attribute on every element). |
| Embedded | `1` | CSS styles are written separately from the content in a style sheet embedded in the HTML file. |
| External | `2` | CSS styles are written separately from the content in a style sheet in an external file. The HTML file links the style sheet. |

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

* property [CssStyleSheetType](../htmlsaveoptions/cssstylesheettype/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
