---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup method
linktitle: get_ExportPageSetup
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup method. Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is false in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Remarks


Each [Section](../../../aspose.words/section/) in Aspose.Words document model provides page setup information via [PageSetup](../../../aspose.words/pagesetup/) class. When you export a document to HTML format you might need to keep this information for further usage. In particular, page setup might be important for rendering to paged media (printing) or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature is inactive by default. 
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
