---
title: Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType method
linktitle: get_CssStyleSheetType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType method. Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is Inline for HTML/MHTML and External for EPUB in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheettype/
---
## HtmlSaveOptions::get_CssStyleSheetType method


Specifies how CSS (Cascading [Style](../../../aspose.words/style/) Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [Inline](../../cssstylesheettype/) for HTML/MHTML and [External](../../cssstylesheettype/) for EPUB.

```cpp
Aspose::Words::Saving::CssStyleSheetType Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType() const
```

## Remarks


[Saving](../../) CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [External](../../cssstylesheettype/), CSS file will be encapsulated into the output package.

## See Also

* Enum [CssStyleSheetType](../../cssstylesheettype/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
