---
title: CssStyleSheetType enumeration
linktitle: CssStyleSheetType enumeration
articleTitle: CssStyleSheetType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.CssStyleSheetType enumeration. Specifies how CSS (Cascading Style Sheet) styles are exported to HTML."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/cssstylesheettype/
---

## CssStyleSheetType enumeration

Specifies how CSS (Cascading Style Sheet) styles are exported to HTML.


### Members

| Name | Description |
| --- | --- |
| Inline | CSS styles are written inline (as a value of the **style** attribute on every element). |
| Embedded | CSS styles are written separately from the content in a style sheet embedded in the HTML file. |
| External | CSS styles are written separately from the content in a style sheet in an external file. The HTML file links the style sheet. |

### Examples

Shows how to work with CSS stylesheets that an HTML conversion creates.

```js
test('ExternalCssFilenames', () => {
  let doc = new aw.Document(base.myDir + "Rendering.docx");

  // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
  // to modify how we convert the document to HTML.
  let options = new aw.Saving.HtmlSaveOptions();

  // Set the "CssStylesheetType" property to "CssStyleSheetType.External" to
  // accompany a saved HTML document with an external CSS stylesheet file.
  options.cssStyleSheetType = aw.Saving.CssStyleSheetType.External;

  // Below are two ways of specifying directories and filenames for output CSS stylesheets.
  // 1 -  Use the "CssStyleSheetFileName" property to assign a filename to our stylesheet:
  options.cssStyleSheetFileName = base.artifactsDir + "SavingCallback.ExternalCssFilenames.css";

  // 2 -  Use a custom callback to name our stylesheet:
  options.cssSavingCallback =
    new CustomCssSavingCallback(base.artifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

  doc.save(base.artifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
});


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
    expect(args.document.originalFileName.EndsWith("Rendering.docx")).toEqual(true);

    args.cssStream = new FileStream(mCssTextFileName, FileMode.create);
    args.isExportNeeded = mIsExportNeeded;
    args.keepCssStreamOpen = mKeepCssStreamOpen;

    expect(args.cssStream.CanWrite).toEqual(true);
  }

  private readonly string mCssTextFileName;
  private readonly bool mIsExportNeeded;
  private readonly bool mKeepCssStreamOpen;
}
```

### See Also

* module [Aspose.Words.Saving](../)
* property [HtmlSaveOptions.cssStyleSheetType](../htmlsaveoptions/cssStyleSheetType/)

