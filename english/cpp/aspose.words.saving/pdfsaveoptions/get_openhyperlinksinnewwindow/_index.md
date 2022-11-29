---
title: get_OpenHyperlinksInNewWindow
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.
type: docs
weight: 274
url: /cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## Remarks


The default value is **false**. When this value is set to **true** hyperlinks are saved using JavaScript code. JavaScript code is **app.launchURL("URL", true);**, where **URL** is a hyperlink.

Note that if this option is set to **true** hyperlinks can't work in some PDF readers e.g. Chrome, Firefox.

JavaScript actions are prohibited by PDF/A-1 and PDF/A-2 compliance. **false** will be used automatically when saving to PDF/A-1 and PDF/A-2.

## Examples



Shows how to save hyperlinks in a document we convert to PDF so that they open new pages when we click on them. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertHyperlink(u"Testlink", u"https://www.google.com/search?q=%20aspose", false);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "OpenHyperlinksInNewWindow" property to "true" to save all hyperlinks using Javascript code
// that forces readers to open these links in new windows/browser tabs.
// Set the "OpenHyperlinksInNewWindow" property to "false" to save all hyperlinks normally.
options->set_OpenHyperlinksInNewWindow(openHyperlinksInNewWindow);

doc->Save(ArtifactsDir + u"PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
