---
title: CssSavingArgs class
linktitle: CssSavingArgs class
articleTitle: CssSavingArgs class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.CssSavingArgs class. Provides data for the [ICssSavingCallback.cssSaving()](../icsssavingcallback/cssSaving/#csssavingargs) event"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/csssavingargs/
---

## CssSavingArgs class

Provides data for the [ICssSavingCallback.cssSaving()](../icsssavingcallback/cssSaving/#csssavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Remarks

By default, when Aspose.Words saves a document to HTML, it saves CSS information inline
(as a value of the **style** attribute on every element).


[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

To save CSS into stream, use the Aspose.Words.Saving.CssSavingArgs.CssStream property.

To suppress saving CSS into a file and embedding to HTML document use the [CssSavingArgs.isExportNeeded](./isExportNeeded/) property.




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the document object that is currently being saved. |
| [isExportNeeded](./isExportNeeded/) | Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is ``true``. When this property is ``false``, the CSS information will not be saved to a CSS file and will not be embedded to HTML document. |
| [keepCssStreamOpen](./keepCssStreamOpen/) | Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information. |

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

