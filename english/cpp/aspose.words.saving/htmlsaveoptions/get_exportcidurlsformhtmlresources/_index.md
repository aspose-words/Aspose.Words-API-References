---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method
linktitle: get_ExportCidUrlsForMhtmlResources
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method. Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is false in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## Remarks


This option affects only documents being saved to MHTML.

By default, resources in MHTML documents are referenced by file name (for example, "image.png"), which are matched against "Content-Location" headers of MIME parts.

This option enables an alternative method, where references to resource files are written as CID (Content-ID) URLs (for example, "cid:image.png") and are matched against "Content-ID" headers.

In theory, there should be no difference between the two referencing methods and either of them should work fine in any browser or mail agent. In practice, however, some agents fail to fetch resources by file name. If your browser or mail agent refuses to load resources included in an MTHML document (doesn't show images or doesn't load CSS styles), try exporting the document with CID URLs. 
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
