---
title: PdfSaveOptions.openHyperlinksInNewWindow property
linktitle: openHyperlinksInNewWindow property
articleTitle: openHyperlinksInNewWindow property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.openHyperlinksInNewWindow property. Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser."
type: docs
weight: 230
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/openHyperlinksInNewWindow/
---

## PdfSaveOptions.openHyperlinksInNewWindow property

Gets or sets a value determining whether hyperlinks in the output Pdf document
are forced to be opened in a new window (or tab) of a browser.


```js
get openHyperlinksInNewWindow(): boolean
```

### Remarks

The default value is ``False``. When this value is set to ``True``
hyperlinks are saved using JavaScript code.
JavaScript code is ``app.launchURL("URL", true);``,
where ``URL`` is a hyperlink.


Note that if this option is set to ``True`` hyperlinks can't work
in some PDF readers e.g. Chrome, Firefox.


JavaScript actions are prohibited by PDF/A-1 and PDF/A-2 compliance. ``False`` will be used automatically when
saving to PDF/A-1 and PDF/A-2.




### Examples

Shows how to save hyperlinks in a document we convert to PDF so that they open new pages when we click on them.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertHyperlink("Testlink", "https://www.google.com/search?q=%20aspose", false);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "OpenHyperlinksInNewWindow" property to "true" to save all hyperlinks using Javascript code
// that forces readers to open these links in new windows/browser tabs.
// Set the "OpenHyperlinksInNewWindow" property to "false" to save all hyperlinks normally.
options.openHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.save(base.artifactsDir + "PdfSaveOptions.openHyperlinksInNewWindow.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

