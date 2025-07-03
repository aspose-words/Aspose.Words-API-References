---
title: Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow method
linktitle: get_OpenHyperlinksInNewWindow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow method. Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser in C++.'
type: docs
weight: 24000
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
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
