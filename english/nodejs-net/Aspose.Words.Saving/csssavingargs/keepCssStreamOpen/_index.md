---
title: CssSavingArgs.keepCssStreamOpen property
linktitle: keepCssStreamOpen property
articleTitle: keepCssStreamOpen property
second_title: Aspose.Words for NodeJs
description: "CssSavingArgs.keepCssStreamOpen property. Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information."
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/csssavingargs/keepCssStreamOpen/
---

## CssSavingArgs.keepCssStreamOpen property

Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information.


```js
get keepCssStreamOpen(): boolean
```

### Remarks

Default is ``false`` and Aspose.Words will close the stream you provided
in the Aspose.Words.Saving.CssSavingArgs.CssStream property after writing an CSS information into it.
Specify ``true`` to keep the stream open.




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

* module [Aspose.Words.Saving](../../)
* class [CssSavingArgs](../)

