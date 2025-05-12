---
title: HtmlSaveOptions.cssStyleSheetFileName property
linktitle: cssStyleSheetFileName property
articleTitle: cssStyleSheetFileName property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.cssStyleSheetFileName property. Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML"
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/cssStyleSheetFileName/
---

## HtmlSaveOptions.cssStyleSheetFileName property

Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document
is exported to HTML.
Default is an empty string.


```js
get cssStyleSheetFileName(): string
```

### Remarks

This property has effect only when saving a document to HTML format
and external CSS style sheet is requested using [HtmlSaveOptions.cssStyleSheetType](../cssStyleSheetType/).

If this property is empty, the CSS file will be saved into the same folder and with the same name as the HTML
document but with the ".css" extension.

If only path but no file name is specified in this property, the CSS file will be saved into the specified
folder and will have the same name as the HTML document but with the ".css" extension.

If the folder specified by this property doesn't exist, it will be created automatically before the CSS file
is saved.

Another way to specify a folder where external CSS file is saved is to use [HtmlSaveOptions.resourceFolder](../resourceFolder/).





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
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.resourceFolder](../resourceFolder/)
* property [HtmlSaveOptions.resourceFolderAlias](../resourceFolderAlias/)
* property [HtmlSaveOptions.cssStyleSheetType](../cssStyleSheetType/)

