---
title: Aspose::Words::Saving::HtmlSaveOptions::set_CssStyleSheetType method
linktitle: set_CssStyleSheetType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::set_CssStyleSheetType method. Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is Inline for HTML/MHTML and External for EPUB in C++.'
type: docs
weight: 54000
url: /cpp/aspose.words.saving/htmlsaveoptions/set_cssstylesheettype/
---
## HtmlSaveOptions::set_CssStyleSheetType method


Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [Inline](../../cssstylesheettype/) for HTML/MHTML and [External](../../cssstylesheettype/) for EPUB.

```cpp
void Aspose::Words::Saving::HtmlSaveOptions::set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType value)
```

## Remarks


Saving CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.
## See Also

* [CssStyleSheetFileName](../get_cssstylesheetfilename/)

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
