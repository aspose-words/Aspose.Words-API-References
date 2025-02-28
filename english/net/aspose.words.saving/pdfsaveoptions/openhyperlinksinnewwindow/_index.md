---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words for .NET
description: Control hyperlink behavior in your PDF with PdfSaveOptions. Easily set links to open in a new window or tab for enhanced user experience.
type: docs
weight: 230
url: /net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Remarks

The default value is `false`. When this value is set to `true` hyperlinks are saved using JavaScript code. JavaScript code is `app.launchURL("URL", true);`, where `URL` is a hyperlink.

Note that if this option is set to `true` hyperlinks can't work in some PDF readers e.g. Chrome, Firefox.

JavaScript actions are prohibited by PDF/A-1 and PDF/A-2 compliance. `false` will be used automatically when saving to PDF/A-1 and PDF/A-2.

## Examples

Shows how to save hyperlinks in a document we convert to PDF so that they open new pages when we click on them.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "OpenHyperlinksInNewWindow" property to "true" to save all hyperlinks using Javascript code
// that forces readers to open these links in new windows/browser tabs.
// Set the "OpenHyperlinksInNewWindow" property to "false" to save all hyperlinks normally.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
