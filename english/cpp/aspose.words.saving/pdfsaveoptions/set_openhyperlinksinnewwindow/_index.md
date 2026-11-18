---
title: Aspose::Words::Saving::PdfSaveOptions::set_OpenHyperlinksInNewWindow method
linktitle: set_OpenHyperlinksInNewWindow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::set_OpenHyperlinksInNewWindow method. Sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser in C++.'
type: docs
weight: 57000
url: /cpp/aspose.words.saving/pdfsaveoptions/set_openhyperlinksinnewwindow/
---
## PdfSaveOptions::set_OpenHyperlinksInNewWindow method


Sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.

```cpp
void Aspose::Words::Saving::PdfSaveOptions::set_OpenHyperlinksInNewWindow(bool value)
```

## Remarks


 The default value is **false**. When this value is set to **true** hyperlinks are saved using JavaScript code. JavaScript code is **app.launchURL("URL", true);**, where **URL** is a hyperlink. 

 Note that if this option is set to **true** hyperlinks can't work in some PDF readers e.g. Chrome, Firefox. 

JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance. The **false** value will be used automatically in this case.
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
